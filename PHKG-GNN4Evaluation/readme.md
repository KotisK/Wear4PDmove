# Evaluating ontology-based PD monitoring and alerting in personal health Knowledge Graphs and Graph Neural Networks

> This folder contains data, code and semantics used to build PHKG and
> GNNs for PD  monitoring/alerting that has been presented in our
> related paper for evaluating the Wear4PDmove ontology.

![PHGNNs](https://github.com/KotisK/Wear4PDmove/assets/56201735/3ca4c55f-9163-4edf-9e47-411e8af80d65)

This architecture can be broken down into three main components:

 1. Data Processing:
 - Data Loader: Represents the component responsible for loading patient health data (real-time apps), which may come from various sources such as electronic health records, mobile devices, etc.
 - Graph Constructor: This component is tasked with constructing a graph from the loaded data (PHKG). The nodes could represent patients, and the edges might represent relationships or interactions between patients or patient features.
 - Ontology (Wear4PDmoveOnto): This indicates the use of a specific ontology (data instances), designed for movement disorders such as Parkinson's disease, as indicated by "PD". Ontologies are used to structure data and knowledge in a specific domain, enabling more efficient data integration, search and analysis.

 2. Neural Network Layers:
 - Attention Mechanism: This component is a part of the GATConv layer, which helps the network focus on the most relevant parts of the input data. It's especially useful in graph data where the significance of nodes and edges can vary greatly.
 - GATConv Layer: Stands for Graph Attention Convolution Layer, which is a type of layer used in Graph Attention Networks. It applies the attention mechanism to graph-structured data.
 - GCNConv Layer: Stands for Graph Convolutional Network Convolution Layer. This layer applies a convolution operation over graphs to capture the topological structure of the data.
 - Activation Function: This is a non-linear function applied after convolution layers. It introduces non-linearity to the model, allowing it to learn more complex patterns.

 3. Training Components:
 - Training Loop: This component represents the iterative process where the model learns from the data by adjusting its weights. It usually involves passing the input data through the network multiple times.
 - Loss Calculation: In each iteration of the training loop, the model's predictions are compared to the true values, and the discrepancy is measured using a loss function. This measure guides the network on how to adjust its weights to improve predictions.
 - Backpropagation: This is the mechanism by which the loss is propagated back through the network, allowing the model to update its weights in a direction that reduces the loss.

In summary, this architecture diagram of the PHGNN provides a high-level view of how patient health data can be processed using graph neural networks to potentially yield insights or predictions about patient health outcomes. The use of both GAT and GCN layers suggests that the network aims to leverage the strengths of both attention mechanisms and convolution operations to analyze graph-structured data effectively.


# Patient Health Graph Neural Networks (PHGNNs)

This repository contains the resources and scripts for creating and analyzing Patient Health Graph Neural Networks (PHGNNs) using Graph Attention Networks (GAT) and Graph Convolutional Networks (GCN) algorithms. Our main ontology, `Wear4PDmoveOnto_v2.owl`, is used in conjunction with several imported ontologies to facilitate comprehensive data analysis and model training.

## Ontologies

### Main Ontology
- `Wear4PDmoveOnto_v2.owl`: The primary ontology developed for representing and analyzing movement data in Parkinson's Disease research.

### Imported Ontologies
- `PMDO_v1.0.owl`: Parkinson's Disease Ontology version 1.0.
- `saref4envi.rdf`: An ontology for the environment in smart applications.
- `sosa.owl`: Ontology based on the SOSA (Sensor, Observation, Sample, and Actuator) model.

## Ontology Analysis

We have used the Protege tool for initial analysis and visualization of the ontologies. Following this, a custom script/mechanism has been developed for further in-depth analysis. The script ensures all imported ontologies are appropriately integrated.

- `ontology_merged_all_scripts_vFINAL.ipynb`: Jupyter notebook containing the analysis mechanism along with instructions for handling the imported ontology files.

## Graph Neural Networks

To achieve the goal of creating PHGNNs, we have developed a script that implements both GAT and GCN algorithms. This script is designed to be flexible, with the capability to generate necessary CSV files automatically if they are not provided.

- `gnn_vFinal.ipynb`: Jupyter notebook that contains the implementation of GNNs for the construction of PHGNNs.

## Data Files

- `output.csv`: Retrieve direct data from our ontology.
- `output_modified.csv`: A modified version of the `output.csv`, which is used as input for the GNN algorithms
- These files are either provided or created by `gnn_vFinal.ipynb`.
