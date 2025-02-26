# Network Sampling and Community Identification

This repository contains a Jupyter Notebook (`Sampling_Network_and_Identify_Communities.ipynb`) that demonstrates how to sample a network, extract its backbone, and evaluate the similarity of community structures using **Normalized Mutual Information (NMI)**. The notebook uses Python and popular libraries such as NetworkX, NumPy, and the Louvain method for community detection to perform network analysis, backbone extraction, and NMI calculations.

---

## Overview

The notebook covers the following steps:
1. **Loading a Network Dataset**: The network is loaded from a file or generated synthetically.
2. **Extracting the Backbone**: Techniques are applied to extract the backbone of the original network, preserving the most significant edges.
3. **Sampling the Network**: A subset of nodes and edges is sampled from the original network or its backbone using a specified sampling method.
4. **Extracting Backbones from Sampled Networks**: The backbone is extracted from each sampled network.
5. **Identifying Communities**: The **Louvain method** is applied to detect communities in:
   - The original network.
   - The backbone of the original network.
   - The sampled networks.
   - The backbones of the sampled networks.
6. **Calculating NMI**: The Normalized Mutual Information (NMI) is computed to compare the community structures of:
   - The original network and its backbone.
   - The original network and the sampled networks.
   - The original network and the backbones of the sampled networks.

---

## Requirements

To run the notebook, you need the following Python libraries installed:
- `networkx` (for network analysis)
- `numpy` (for numerical operations)
- `scikit-learn` (for calculating NMI)
- `python-louvain` (for the Louvain community detection method)

You can install the required libraries using `pip`:

```bash
pip install networkx numpy scikit-learn python-louvain
# Network Sampling and Community Detection

## Usage

### Clone the repository:
```bash
git clone https://github.com/rainara-araujo/network-sampling-communities.git
cd network-sampling-communities
```

### Open the Jupyter Notebook:
```bash
jupyter notebook Sampling_Network_and_Identify_Communities.ipynb
```

### Run the notebook cells step by step to:
1. Load or generate a network.
2. Extract the backbone of the network using techniques such as the **Disparity Filter** or **Global Thresholding**.
3. Sample the network (or its backbone) using a chosen method (e.g., **random node sampling, edge sampling**, etc.).
4. Extract backbones from the sampled networks.
5. Detect communities using the **Louvain method** in:
   - The original network.
   - The backbone of the network.
   - The sampled networks and their backbones.
6. Calculate the **Normalized Mutual Information (NMI)** to compare community structures.

## Dataset
The notebook is designed to work with any network dataset in the form of an **edge list** or **adjacency matrix**. You can replace the example dataset with your own by modifying the data loading section of the notebook.

## Backbone Extraction Techniques
The notebook demonstrates the use of the following backbone extraction techniques:

- **Disparity Filter**: Retains edges that are statistically significant based on the local topology of the network.
- **Global Thresholding**: Retains edges with weights above a specified threshold.

These techniques help reduce the complexity of the network while preserving its most important structural features.

## Sampling Methods
The notebook supports the following sampling methods:

- **Random Node Sampling**: Randomly selects a subset of nodes and includes all edges between them.
- **Random Edge Sampling**: Randomly selects a subset of edges.
- **Snowball Sampling**: Starts with a seed node and iteratively adds neighbors to the sample.

## Community Detection and NMI Calculation
The **Louvain method** is used to detect communities in:

- The original network.
- The backbone of the original network.
- The sampled networks.
- The backbones of the sampled networks.

### NMI Calculation
The **Normalized Mutual Information (NMI)** is then calculated to evaluate the similarity between the community structures of:

- The original network and its backbone.
- The original network and the sampled networks.
- The original network and the backbones of the sampled networks.

NMI is a metric that ranges from **0 (no similarity)** to **1 (identical community structures)**.

## Contributing
Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an **issue** or submit a **pull request**.

