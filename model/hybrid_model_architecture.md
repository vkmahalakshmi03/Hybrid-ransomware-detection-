# Hybrid Detection Model — Architecture

## Model Design

[File Input]
     │
     ▼
┌─────────────────────────┐
│  STAGE 1                │
│  Signature-Based Scan   │  ──── MATCH ──→ [ALERT: Known Ransomware]
│  (Hash + Pattern DB)    │
└─────────────────────────┘
     │ NO MATCH
     ▼
┌─────────────────────────┐
│  STAGE 2                │
│  ML Behavioral Analysis │  ── MALICIOUS → [ALERT: Novel Variant]
│  Random Forest /        │
│  Gradient Boosting      │
└─────────────────────────┘
     │ CLEAN
     ▼
┌─────────────────────────┐
│  STAGE 3                │
│  Ensemble Decision      │  → Final Verdict: CLEAN or RANSOMWARE
└─────────────────────────┘

## Behavioral Features (Stage 2 Inputs)

- File entropy measurement (post-modification)
- File rename/extension change rate
- Registry modification patterns
- API call sequences
- Network connection behavior (C2 indicators)

## Design Rationale

| Decision | Reason |
|---|---|
| Signature first | Low computational cost — fast elimination of known threats |
| ML second | Handles zero-day and polymorphic variants signature DB misses |
| Ensemble output | Either detection = threat → minimizes false negatives |
| Cloud-ready architecture | Stateless per-file processing scales horizontally |

