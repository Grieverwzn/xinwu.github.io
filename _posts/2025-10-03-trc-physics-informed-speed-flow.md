---
layout: single
title: "New paper in TR-C: physics-informed speed-flow prediction"
date: 2025-10-03 12:00:00 +0000
categories: research updates
author: Xin (Bruce) Wu
header:
  teaser: /assets/images/home/tile_la.jpg
---

We embed a calibratable S-shaped three-parameter (S3) traffic stream model into a deep learning framework (multi-graph convolution + LSTM) on a unified computational graph, so network-wide speed and flow predictions stay consistent with traffic flow theory even with missing data.

{% include figure image_path="/assets/images/research/mobility/piml_la_map.jpg" alt="Prediction errors across Los Angeles freeway sensors." caption="Prediction errors across Los Angeles freeway sensors." popup=true %}

**Citation:** Shao, F., Shao, H., **Wu, X.** (corresponding), Cheng, Q., Lam, W.H.K. (2025). A physics-informed machine learning framework for speed-flow prediction: Integrating an S-shaped traffic stream model with deep learning models. *Transportation Research Part C*, 180, 105362. [DOI](https://doi.org/10.1016/j.trc.2025.105362)

More on the [Mobility Data & Traffic System Modeling]({{ '/data-traffic-modeling/' | relative_url }}) page.
