# Detection Methods Comparison — Survey Analysis

## Papers Surveyed: 20+  
## Methodologies Covered: Signature-Based | Behavior-Based | Machine Learning | Hybrid

---

## Signature-Based Detection

| Study | Key Finding | Limitation |
|---|---|---|
| Moser et al. (2007) | Established baseline for signature matching | Cannot detect zero-day variants |
| Bayer et al. (2014) | Identified real-time signature update gaps | Database maintenance challenge |

---

## Behavior-Based Detection

| Study | Approach | Limitation |
|---|---|---|
| Zhao et al. (2018) | Runtime behavior tracking — encryption patterns | High false positives from legitimate processes |
| Sharma et al. (2020) | Behavioral flags in real-time environments | Reduced accuracy under latency constraints |
| Arabo et al. (2020) | Process behavior analysis | Computational overhead |
| Madanayaka et al. (2023) | Proactive behavioral alerting | Rule dependency |

---

## Machine Learning-Based Detection

| Study | Algorithm(s) Used | Key Result |
|---|---|---|
| Yang et al. (2019) | SVM, Decision Trees | Good accuracy; high FP rate |
| Xie et al. (2020) | Deep Learning / Neural Networks | Strong detection; high compute cost |
| Daku et al. (2018) | ML classification of ransomware variants | Effective variant identification |
| Ferdous et al. (2024) | AI-based comprehensive review | Highlights AI gap in unknown threat detection |
| Smith et al. (2022) | Multiple ML frameworks | Framework comparison across detection types |

---

## Hybrid / Ensemble Approaches

| Study | Combination Used | Outcome |
|---|---|---|
| Aljubory & Khammas (2021) | Evolutionary + feature vector | Improved detection feature selection |
| Masum et al. (2022) | ML classification ensemble | Higher accuracy in ransomware classification |
| Srivastava et al. (2023) | ML + Hidden Markov Model | Network-behavior detection improvement |

---

## Summary: Gap Identified

No single method adequately addresses:
1. Novel variant detection (gap in signature-based)
2. Real-time performance (gap in deep learning)
3. False positive reduction (gap in behavior-based)

→ Hybrid model proposed to bridge these three gaps simultaneously.
