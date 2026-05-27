# Hybrid Ransomware Detection: A Survey of Current Technologies

**Research Project | George Mason University | AIT 682 – Network and Systems Security**  
**Author:** Mahalakshmi Karthikeyan

---

## Overview

This research analyzes the evolution of ransomware detection methodologies and proposes a hybrid detection model that combines signature-based and machine learning-driven behavioral analysis to address the shortcomings of standalone approaches.

The study surveyed 20+ ransomware detection research papers across three core detection paradigms and synthesized findings into a multi-stage hybrid detection framework.

---

## Research Problem

Traditional signature-based detection methods fail against:
- Zero-day ransomware variants
- Polymorphic and evolving ransomware strains
- Ransomware-as-a-Service (RaaS) platforms with rapid mutation cycles

Machine learning approaches alone suffer from:
- High false positive rates
- Real-time detection latency
- Large labeled dataset requirements

---

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
