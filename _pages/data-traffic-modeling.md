---
title: "Mobility Data & Traffic Network Modeling"
permalink: /data-traffic-modeling/
layout: single
author_profile: true
---

## Computational graph-based travel demand modeling 

Aiming to develop a theoretically consistent framework to estimate travel demand using multiple data sources, this paper first proposes a multi-layered Hierarchical Flow Network (HFN) representation to structurally model different levels of travel demand variables including trip generation, origin/destination matrices, path/link flows, and individual behavior parameters. Different data channels from household travel surveys, smartphone type devices, global position systems, and sensors can be mapped to different layers of the proposed network structure. We introduce Big data-driven Transportation Computational Graph (BTCG), alternatively Beijing Transportation Computational Graph, as the underlying mathematical modeling tool to perform automatic differentiation on layers of composition functions. A feedforward passing on the HFN sequentially implements 3 steps of the traditional 4-step process: trip generation, spatial distribution estimation, and path flow-based traffic assignment, respectively. BTCG can aggregate different layers of partial first-order gradients and use the back-propagation of “loss errors” to update estimated demand variables. A comparative analysis indicates that the proposed methods can effectively integrate different data sources and offer a consistent representation of demand. The proposed methodology is also evaluated under a demonstration network in a Beijing subnetwork
