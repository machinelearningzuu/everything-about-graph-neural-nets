# everything-about-gnns

## Introduction

This repository contains a collection of resources about Graph Neural Networks (GNNs). The resources are organized into the following categories:

        1. Node Classification
        2. Link Prediction
        3. Graph Classification
        4. Graph Generation
        5. Graph Clustering (Community Detection)
        6. Graph Matching
        7. Graph Embedding
        8. Graph Visualization
        9. Graph Sampling


Also we talk about different types of GNNs,

        1. Graph Convolutional Networks (GCNs)
        2. Graph Attention Networks (GATs)
        3. GraphSAGE
        4. Graph Isomorphism Networks (GINs)
        5. Graph U-Nets
        6. Graph Transformer Networks (GTNs)
        7. Graph Recurrent Networks (GRNs)
        8. Graph Variational Autoencoders (GVAEs)
        9. Graph Autoencoders (GAEs)v
        10. Graph Convolutional Matrix Completion (GC-MC)
    

different types of applications of GNNs,

        1. Recommendation Systems
        2. Molecular Property Prediction
        3. Drug Discovery
        4. Social Network Analysis
        5. Fraud Detection
        6. Query Detection

## Graph Data vs Other Data Formats

#### Difference 1 : Size and Shape </br>
- We can configure all data for same size in other data formats such as Images, Videos, Text by Resizing, Cropping & Padding. **Such Operations not defines in Graph Data because of it's complex structure.**
- If you have additional nodes & edges you **can't simply remove them.**
- So it should capable of handling **Graphs with different size.**