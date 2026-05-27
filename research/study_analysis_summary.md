# Study Analysis Summary

## Scope

20+ ransomware detection research papers reviewed across three detection paradigms.  
Publication range: 2018 – 2024.  
Sources: IEEE Access, IEEE conference proceedings, Procedia Computer Science, Future Generation Computer Systems.

---

## What the Literature Gets Right

**Signature-based detection is fast and precise — for what it knows.**  
Every paper that included signature-based methods confirmed high accuracy against known variants with minimal compute overhead. The problem isn't the method, it's the assumption that threat databases stay current against adversaries who deliberately mutate code.

**ML models generalize well when trained on representative data.**  
Random Forest and Gradient Boosting consistently outperformed deep learning models in resource-constrained environments. Deep learning showed stronger pattern recognition but required substantially more training data and compute — a tradeoff that matters in real deployment.

**Behavioral detection catches what signatures miss.**  
Studies tracking file I/O patterns, entropy spikes, and API call sequences detected ransomware activity that had no signature match. The limitation is environmental noise — legitimate processes like backup software or compression tools trigger the same behavioral flags.

---

## Where the Literature Falls Short

**Almost no paper addressed operational deployment constraints.**  
Detection accuracy was the dominant metric across reviewed studies. Latency, compute cost, and integration with existing SIEM or EDR platforms were rarely discussed. A model that performs well in a lab environment and adds 800ms per file scan is not deployable at enterprise scale.

**Dataset diversity is a persistent problem.**  
Several ML-based studies trained and tested on the same ransomware family datasets — CIC, VirusShare, VirusTotal samples. Detection rates look strong until the model encounters a variant family not represented in training data. This is the exact scenario that matters most in practice.

**Hybrid approaches were underexplored relative to their potential.**  
Of the 20+ papers reviewed, fewer than a third proposed or tested hybrid models. Those that did showed consistent improvements over standalone methods — lower false positive rates, better zero-day coverage — but hybrid design was treated as a future direction rather than a current implementation priority.

---

## Pattern Across All Three Methodologies

| Finding | Signature-Based | Behavior-Based | ML-Based |
|---|---|---|---|
| Strong against known variants | ✓ | Partial | Partial |
| Handles zero-day threats | ✗ | ✓ | ✓ |
| Low false positive rate | ✓ | ✗ | Varies |
| Real-time capable | ✓ | Partial | Depends on model |
| Scalable to enterprise | ✓ | ✗ | Depends on architecture |

No single method checks all five. That's the gap the hybrid model addresses.

---

## Research Direction This Informed

The consistent failure pattern across reviewed studies — good accuracy in isolation, poor coverage across threat types — directly shaped the hybrid model design. The decision to use signature scanning as a first-pass filter came from observing how much compute behavioral and ML methods spend on files that a signature check would have resolved in milliseconds.

The ensemble decision logic (flag if either method triggers) was chosen specifically because the reviewed literature showed false negatives are the more dangerous failure mode in ransomware detection — a missed threat causes damage; a false positive causes an alert.
