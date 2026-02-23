Hybrid Digital Twin-Federated Learning IDS (DT-FL-IDS)
Azra Fathima and Naren Kumar

Privacy-preserving intrusion detection framework achieving state-of-the-art robustness against Non-IID data distributions and zero-day attacks in IoT environments.

Performance on CICIDS2017 Dataset
Metric	DT-FL Hybrid	Standalone FL	Centralized LSTM
F1 Score	0.94	0.72	0.91
Recall	0.97	0.85	0.93
False Positive Rate	0.19	0.35	0.22
Drift Degradation	3.75x slower	Baseline	2.1x slower
Technical Contributions
Novel Hybrid Decision Architecture

Per-client Digital Twin autoencoders learn device-specific normal behavior. Reconstruction errors gate federated classifier decisions using 95th-percentile thresholding, suppressing false positives while maintaining high recall against novel attacks.

Non-IID Simulation Framework

10-client partitioning with attack-skewed (90% attack), benign-skewed (90% benign), and balanced distributions. FedAvg aggregation maintains convergence despite extreme label skew.

Production-Ready Fusion Logic

text
IF reconstruction_error(x) > T_p (client-specific):
    ANOMALY  # Zero-day detection
ELSE:
    FL_classifier(x)  # Known attack/benign
T_p = percentile(benign_recon_errors, 95%)

Repository Organization
text
literature/              # 10+ related works (Salim2024, IEEE papers)
methodology/             # Problem formulation + hybrid logic + Non-IID setup
experiments/             # Full ablation studies + baseline comparisons
├── experimental_setup.md
├── results_main.md
└── ablation_study.md
Research Context
Addresses three critical gaps in IoT cybersecurity:

Privacy-preserving learning across heterogeneous edge devices

Robustness degradation under distribution drift

Zero-day attack detection beyond supervised capabilities

Implementation validates 30% F1 improvement over federated baselines while preserving edge privacy. Framework generalizes to any time-series anomaly detection task.

Manuscript Status
IEEE-format LaTeX draft complete and undergoing internal review. Methodology and experiments fully documented for reproducibility.
