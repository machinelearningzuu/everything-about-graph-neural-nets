# everything-about-gnns

## A] Introduction

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

## B] Graph Data vs Other Data Formats

#### Difference 1 : Size and Shape </br>
- We can configure all data for same size in other data formats such as Images, Videos, Text by Resizing, Cropping & Padding. **Such Operations not defines in Graph Data because of it's complex structure.**
- If you have additional nodes & edges you **can't simply remove them.**
- So it should capable of handling **Graphs with different size.**

#### Difference 2 : Isomorphism </br>
- Graph Data isomorphism is defined by **Graph Structure.** 2 graphs that look different can still be structurally identical.
- This doesn't work on other data types. ex: if you flip an image, it's not same as the original one, it's different.
- **But if you flip a graph only thing change is order of the nodes. In this case the algorithms suppose to handle graph data should be permutation invariant**
- This is the reason why you can't use Adjacency Matrix as the input data for GNNs, because it's sensitive to node ordering. which means **A GRAPH WITH DIFFERENT 2 NODE ORDEING SETTINGS RESULTS IN 2 DIFFERENT ADJACENCY METRICES.** So Adjancent Matrix is not Permutaion Invariant

#### Difference 3 : Grid Structure </br>
- Graphs are dynamic strctures. they can't simply represent as X, Y coordinates. You can't really say 2 nodes are closed to each other if they locate nearby. It rely on both node attributes & edge attributes. 


## C] Idealogy of GNNs
- Learning a neural network by suitable representation of graph data a.k.a **Representation Learning**
- The main objective of GNN is to find **Node/Graph Embedding** using data stores in the graph such as Node features, Edge features.
- Intuition -> **# Representation Learning === Extract Node/Graph Embedding**

#### How Graph Neural Networks work ?
- Core building blocks of GNN is **Message passing Layers**. They are responsible for combining Edge / Node Features into Node / graph Embeddings. 
- The way this happens can be exposed by **Graph Convolution.** The typical convolution concept represented by ConvNets extended here. Instead of Sliding kernal approach here it introduce the concept of **Node's Neighbourhood**. Using this approach **GNN can evaluate how neighbouring nodes keeps & share their information and this is called "Message Passing"**

![How Message Passinng Works ?](https://github.com/1zuu/everything-about-gnns/blob/main/git-vis/message-passing.png)

- Message Passing can be more easily elaborate through **Computational Graph Representation**

![How Message Passinng Works ?](https://github.com/1zuu/everything-about-gnns/blob/main/git-vis/computaional-graph.png)

##### Number of Layers of the GNN === Number of Neighbourhood-Hops we perform


## D] Variants of GNN
- Based on **How message passing updates & Aggregation Function works** we can derive different variants of GNN 

![How Message Passinng Works ?](https://github.com/1zuu/everything-about-gnns/blob/main/git-vis/gnn-variants.png)
