# Hybrid Ransomware Detection: A Survey of Current Technologies

**Research Project | George Mason University | AIT 682 – Network and Systems Security**  
**Author:** Mahalakshmi Karthikeyan

---

## Overview

Ransomware has moved from opportunistic attacks to coordinated, targeted campaigns. 
LockBit 3.0 disrupted global logistics and healthcare networks throughout 2023. 
BlackCat/ALPHV brought down Change Healthcare in 2024, impacting 100+ million patient 
records. WannaCry and the Colonial Pipeline attack demonstrated how a single intrusion 
can cascade across critical infrastructure.

What these incidents share — the detection systems in place failed to catch novel 
variants early enough. This research examines why, and proposes a hybrid detection 
model that addresses the core gap.

I reviewed 20+ ransomware detection studies across three methodologies — 
signature-based, behavioral, and machine learning — and found a consistent pattern: 
no single approach handles both known variants and zero-day threats without trading 
off real-time performance or false positive rates.

---

## Research Problem

The three failure points that existing detection systems don't solve together:

- **Signature-based methods** fail against new and polymorphic variants — LockBit 
  alone has released multiple versions specifically designed to evade signature databases
- **Behavior-based methods** generate excessive false positives when legitimate 
  processes mirror ransomware activity (mass file operations, encryption tasks)
- **ML models** struggle with real-time detection and require large labeled datasets 
  that rarely reflect the latest ransomware families

## Proposed Hybrid Detection Model

The model operates in three stages:

| Stage | Method | Purpose |
|---|---|---|
| Stage 1 | Signature-Based Scan | Rapid detection of known ransomware variants |
| Stage 2 | ML Behavioral Analysis | Detection of novel/zero-day variants via pattern recognition |
| Stage 3 | Ensemble Decision | Combined output to minimize false negatives |

**ML Algorithms analyzed:** Random Forest, Gradient Boosting, SVM, Decision Trees  
**Behavioral Indicators monitored:** Mass file encryption, unauthorized file access, abnormal I/O patterns

---

## Detection Methodology Comparison

| Approach | Strengths | Limitations |
|---|---|---|
| Signature-Based | Fast, accurate for known threats | Ineffective against new/polymorphic variants |
| Heuristic / Behavior-Based | Detects unknown behavior | High false positives, computational overhead |
| Machine Learning | Adaptive, pattern-based | Requires labeled data, real-time latency |
| **Hybrid (Proposed)** | **Comprehensive coverage, lower FP rate** | **Complexity of integration** |

---

## Key Findings

- Hybrid models outperform standalone detection methods in detection rate and false positive reduction
- ML-based behavioral analysis (Random Forest, Gradient Boosting) effectively captures novel ransomware patterns
- Signature-based scanning provides a low-cost first filter, reducing ML model load
- Architecture is scalable for cloud-based enterprise environments

---

## MITRE ATT&CK Alignment

Ransomware techniques addressed in this research map to:

| Tactic | Technique | ID |
|---|---|---|
| Impact | Data Encrypted for Impact | T1486 |
| Defense Evasion | Obfuscated Files or Information | T1027 |
| Execution | User Execution: Malicious File | T1204.002 |
| Command & Control | Encrypted Channel | T1573 |

---

## Repository Contents
├── paper/          → Full research paper (AIT 682)
├── research/       → Detection method analysis and study summary
├── model/          → Hybrid model architecture and detection logic
└── references/     → Annotated bibliography of 20 surveyed papers

---

## Skills Demonstrated

`Threat Analysis` · `MITRE ATT&CK` · `Machine Learning in Security` · `Security Research` · `Incident Detection` · `Behavioral Analysis` · `SIEM-aligned Detection Logic`

---

## Academic Context

- **Course:** AIT 682 – Network and Systems Security  
- **Institution:** George Mason University  
- **Advisor:** Dr. Kun Sun  
- **Year:** 2025
