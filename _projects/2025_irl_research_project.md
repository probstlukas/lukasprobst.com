---
layout: page
title: Explainable AI for Robot Action Predictions
description: Research practical on graph-based explanations for imitation learning in robotics
img: assets/img/projects/irl_research_project/GNNExplainer_no_node_mask.jpg
importance: 1
category: uni
related_publications: false
---

## Overview

As part of a research practical at KIT’s [Intuitive Robots Lab (IRL)](https://www.irl.iar.kit.edu/), I worked on explaining robot action predictions in imitation learning using graph-based methods. The project focused on making graph neural network predictions more transparent in robotic manipulation settings by analyzing which parts of the graph structure were most influential for the model’s decisions.

We evaluated several graph explainability methods (GNNExplainer, PGExplainer, and AttentionExplainer) in the context of robotic imitation learning. The experiments were conducted in the [RoboCasa simulation framework](https://www.irl.iar.kit.edu/) on a drawer-closing task, combining both quantitative evaluation and qualitative embedding analysis.

## What I worked on

My work centered on investigating how graph embeddings and explainability techniques can be used to better understand robot behavior in imitation learning pipelines. This included:

- applying graph explainability methods to robotic action prediction models,
- analyzing learned graph embeddings with dimensionality reduction techniques such as PCA, UMAP, and t-SNE,
- quantitatively evaluating explanations using adapted fidelity and Euclidean distance metrics for regression tasks,
- and comparing different explanation methods on train and test trajectories.

## Project setting

The project uses Graph Neural Networks (GNNs) to model structured relationships in robotic environments and applies explainability methods to identify the nodes, edges, and subgraphs most relevant for a robot’s predicted actions. The benchmark task was CloseDrawer in RoboCasa, a household manipulation environment designed for evaluating robotic agents.

## Main results

Across the evaluated explainers, PGExplainer achieved the strongest quantitative results, showing the highest fidelity scores and the lowest Euclidean distances on both train and test trajectories. AttentionExplainer also performed well and offered a computationally efficient alternative by leveraging built-in attention coefficients from the model. In contrast GNNExplainer with node masking substantially reduced explanation quality, highlighting the importance of node features in the model’s decision process.

On the embedding analysis side, the dimensionality-reduction experiments showed that the learned trajectory embeddings formed meaningful path-like structures. t-SNE was particularly effective at preserving local and global relationships in the embeddings, while the reduced trajectories also visually aligned with the robot end-effector motion.

## Takeaways

This project gave me hands-on experience at the intersection of:

- robot learning
- graph neural networks
- explainable AI
- representation analysis
- quantitative evaluation for interpretable ML systems

More broadly, it reinforced my interest in building machine learning systems that are not only performant, but also interpretable and trustworthy in real-world robotic settings.

## Report

You can read the full project report here:

- [Project Report (PDF)](/assets/pdf/2025_Praktikum_IRL_Córcoles_Probst.pdf)

## Project context

This project was completed at Karlsruhe Institute of Technology (KIT) as part of the Research Practical Course: Explainable Artificial Intelligence module.
