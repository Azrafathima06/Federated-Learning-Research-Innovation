# Experimental Setup

## Datasets
- **ToN_IoT**: 22M IoT flows, 46 features, 9 attack types
- Train/Test: 80/20 stratified split
- Non-IID partitioning: 10 clients (code in `data/non_iid_split.py`)

## Baselines
| Model | Description |
|-------|-------------|
| Standalone FL | FedAvg + LSTM classifier |
| Standalone DT | VAE reconstruction only |
| Centralized LSTM | Oracle (all data pooled) |

## Hyperparameters
