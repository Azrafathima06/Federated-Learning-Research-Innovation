Hybrid Digital Twin – Federated Learning Intrusion Detection System (DT-FL-IDS)
Privacy-preserving and drift-resistant intrusion detection framework for heterogeneous IoT environments.
Digital Twin-Gated Federated IDS for IoT  Hybrid FL + DT reconstruction. CICIDS2017: F1 0.94 (+30% vs FL), Recall 0.97, FPR 0.19. 3.75x drift resistance. DT-gated fusion.  Production IoT cybersecurity.
Overview
This repository contains the implementation of a hybrid Digital Twin assisted Federated Learning Intrusion Detection System designed to address two fundamental challenges in IoT security:
Non-IID distributed data across edge devices
Failure of supervised IDS models under unseen attack distributions
The proposed framework integrates:
Federated supervised classifiers → detect known attacks
Digital Twin behavioral autoencoder → detect unknown anomalies
Percentile-based fusion gating → suppress false alarms and improve robustness
The hybrid decision mechanism enables reliable detection of both known and previously unseen cyber threats while preserving data privacy at the edge.
Motivation
IoT deployments generate highly heterogeneous traffic patterns and operate under strict privacy constraints. Traditional centralized IDS cannot scale, and standalone federated learning models degrade under distribution drift. Meanwhile, anomaly detectors lack attack specificity.
This project combines behavioral reconstruction modeling with collaborative learning to achieve:
Privacy preservation
Drift robustness
Reduced false positive rate
Detection of zero-day attacks
Architecture
Pipeline
Edge devices train local supervised IDS models
Behavioral Digital Twin learns normal traffic representation
Reconstruction error percentile computed per device
Federated aggregation updates global model
Hybrid gating combines classifier confidence + anomaly confidence
Final intrusion decision generated
| Metric              | Hybrid DT-FL             | FL Only        |
| ------------------- | ------------------------ | -------------- |
| F1 Score            | 0.94                     | Lower baseline |
| Recall              | 0.97                     | Lower          |
| False Positive Rate | 0.19                     | High           |
| Drift Stability     | 3.75× slower degradation | —              |
