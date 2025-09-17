# DeCentralized_Federated_Learning_with_Blockchain
Federated Learning with Blockchain-Inspired Consensus and HSIC Auditing

This repository contains a modular implementation of a federated learning (FL) framework with the following features:

Clustering & Consensus: Edge nodes aggregate client updates with FedAvg, coordinate-wise median, or Krum.

HSIC Auditing: Post-aggregation independence test using the Hilbert–Schmidt Independence Criterion (HSIC) with permutation testing.

Malicious Clients: Simulation of adversarial participants contributing poisoned/random updates.

Non-IID Data Splitting: Clients receive non-iid datasets using a Dirichlet distribution.

Blockchain-inspired integrity: Each client update is signed and verified before aggregation.

This code is structured for research prototyping, reproducibility, and extension into publishable results.

1. Clone this repository
git clone https://github.com/yourusername/federated_blockchain_FL.git
cd federated_blockchain_FL

2. Install dependencies
pip install -r requirements.txt


Dependencies:

torch – PyTorch deep learning framework

numpy – Numerical computations

scipy – HSIC kernel computations

pytz – Timezone support

~Running the Simulation
Run a simple smoke test (synthetic dataset)
python simulation.py


Expected output:

Running smoke simulation...
Edge 0 aggregated vector length: 101770
Edge 1 aggregated vector length: 101770
HSIC observed: 0.055665, threshold: 0.115800


This verifies that:

Clients train locally

Updates are signed & aggregated

Edge nodes accept/reject updates

HSIC test runs successfully

~Extending Experiments

Use Real Datasets

Replace generate_synthetic_dataset in data_utils.py with torchvision.datasets.CIFAR10 or FashionMNIST.

Keep dirichlet_split for non-IID distribution.

Run Multi-Round Training

Extend simulation.py with a loop over multiple communication rounds.

Track global accuracy/loss after each round.

Baselines to Compare Against

FedAvg (already implemented)

Coordinate-wise Median (robust to outliers)

Krum (Byzantine-resilient)

(Optional) Add FedProx / Bulyan

Malicious Clients

Control fraction of malicious clients via malicious_ids in simulation.py.

Experiment with different attack models (random updates, label flipping, scaling).

Evaluation Metrics

Accuracy / Loss

Communication cost (size of updates × rounds)

Convergence speed

HSIC detection rate for malicious clients

Aggregation robustness

~ Citation

If you use this framework in your research, please cite ():

@article{BhavyaChauhan2025federated,
  title={Blockchain-Assisted Federated Learning with HSIC Auditing for Malicious Client Detection},
  author={Bhavya Chauhan},
  year={2025},
  conderence={Under Submission}
}
