# DeCentralized_Federated_Learning_with_Blockchain
Federated Learning with Blockchain-Inspired Consensus and HSIC Auditing

This repository contains a modular implementation of a federated learning (FL) framework with the following features:

Clustering & Consensus: Edge nodes aggregate client updates with FedAvg, coordinate-wise median, or Krum.

HSIC Auditing: Post-aggregation independence test using the Hilbert–Schmidt Independence Criterion (HSIC) with permutation testing.

Malicious Clients: Simulation of adversarial participants contributing poisoned/random updates.

Non-IID Data Splitting: Clients receive non-iid datasets using a Dirichlet distribution.

Blockchain-inspired integrity: Each client update is signed and verified before aggregation.

This code is structured for research prototyping, reproducibility, and extension into publishable results.
