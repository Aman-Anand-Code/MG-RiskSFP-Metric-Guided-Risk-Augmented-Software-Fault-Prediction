# MG-RiskSFP: Metric-Guided Risk-Augmented Software Fault Prediction

MG-RiskSFP is a lightweight and explainable software fault prediction framework. The project predicts fault-prone software modules by combining traditional software metrics with metric-guided structural risk indicators. The framework is evaluated on publicly available PROMISE software defect prediction datasets using imbalance-aware learning and machine learning classifiers.

## Overview

Software fault prediction helps identify software modules that are likely to contain faults before testing and release. Traditional models often rely only on raw software metrics such as LOC, WMC, CBO, RFC, LCOM, DIT, and related object-oriented metrics. Although these metrics are useful, they are not always directly interpretable.

This project proposes a risk-augmented representation where software metrics are converted into interpretable risk indicators such as:

- Module-size risk
- Code-complexity risk
- Coupling risk
- Cohesion risk
- Inheritance-related risk
- Encapsulation risk

These generated risk indicators are combined with the original software metrics and evaluated using machine learning classifiers under class imbalance.

## Proposed Method

The main proposed feature representation is:

```text
METRICS_RISK = Original Software Metrics + Generated Risk Indicators
