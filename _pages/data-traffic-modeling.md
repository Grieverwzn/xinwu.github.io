---
layout: single
title: "Mobility Data & Traffic System Modeling"
permalink: /data-traffic-modeling/
author_profile: true
toc: true
toc_sticky: true
toc_label: "Research Threads"
excerpt: "Interpretable AI in transportation modeling, emerging data (LBS, climate, health), and transportation multi-resolution modeling & world models."
header:
  overlay_image: /assets/images/research/banner_mobility.jpg
  overlay_filter: 0.55
  caption: "Network-wide speed–flow prediction errors on Los Angeles freeways (Shao et al., 2025, TR-C)"
gallery_cg:
  - image_path: /assets/images/research/mobility/cg_layered_graph.jpg
    title: "(a) Four-step model as a layered computational graph: trip generation, distribution, path flow and link flow layers, calibrated by backpropagation against survey, mobile-phone, floating-car and sensor data"
  - image_path: /assets/images/research/mobility/cg_node_graph.jpg
    title: "(b) Node-level view: forward values and partial derivatives of a logit choice model on the computational graph"
gallery_iml:
  - image_path: /assets/images/research/mobility/cg_policy_levers.jpg
    title: "(c) Congestion-mitigation strategies as levers on the graph: pricing, workplace relocation, population transfer, infrastructure and information"
  - image_path: /assets/images/research/mobility/cg_marginal_effects.jpg
    title: "(d) Marginal-effect analysis of six strategies: change in link flows and travel time"
  - image_path: /assets/images/research/mobility/cg_policy_beijing.jpg
    title: "(e) Beijing subnetwork: estimated travel demand, path flows and link flows"
gallery_piml:
  - url: /assets/images/research/mobility/pinn_concept.jpg
    image_path: /assets/images/research/mobility/pinn_concept.jpg
    alt: "Multi-source detectors and continuous space-time traffic state"
    title: "Fusing loop, probe, Bluetooth, and video data into a continuous space–time traffic state"
  - url: /assets/images/research/mobility/pinn_speed_heatmaps.jpg
    image_path: /assets/images/research/mobility/pinn_speed_heatmaps.jpg
    alt: "Speed estimation heatmaps"
    title: "Reconstructed congestion waves: proposed PINN vs. PeMS smoothing"
  - url: /assets/images/research/mobility/piml_architecture.jpg
    image_path: /assets/images/research/mobility/piml_architecture.jpg
    alt: "PIML architecture with MGCN, LSTM and S3 traffic stream model"
    title: "PIML architecture: MGCN + LSTM learners regulated by the S3 traffic stream model"
  - url: /assets/images/research/mobility/piml_la_map.jpg
    image_path: /assets/images/research/mobility/piml_la_map.jpg
    alt: "Prediction error map on Los Angeles freeway sensors"
    title: "Network-wide prediction errors on Los Angeles freeway sensors"
gallery_mrm:
  - url: /assets/images/research/mobility/mrm_virtual_queue.jpg
    image_path: /assets/images/research/mobility/mrm_virtual_queue.jpg
    alt: "Virtual queue and spatial queue profile at a bottleneck"
    title: "Virtual vs. spatial queue at a bottleneck"
  - url: /assets/images/research/mobility/mrm_i405.jpg
    image_path: /assets/images/research/mobility/mrm_i405.jpg
    alt: "I-405 northbound bottleneck and speed profile"
    title: "I-405 Northbound bottleneck: observed space–time congestion"
  - url: /assets/images/research/mobility/mrm_vc_calibration.jpg
    image_path: /assets/images/research/mobility/mrm_vc_calibration.jpg
    alt: "Queue-based vs. density- and volume-based capacity estimates"
    title: "Queue-based (QBM) vs. density-based (DBM) and volume-based (VBM) V/C calibration"
gallery_lbs:
  - url: /assets/images/research/mobility/lbs_hurricane_laura.jpg
    image_path: /assets/images/research/mobility/lbs_hurricane_laura.jpg
    alt: "Counties affected by Hurricane Laura"
    title: "Hurricane Laura (2020): affected counties"
  - url: /assets/images/research/mobility/lbs_laura_results.jpg
    image_path: /assets/images/research/mobility/lbs_laura_results.jpg
    alt: "Estimated effect on new COVID-19 cases"
    title: "Estimated impact of evacuation-driven mobility on new COVID-19 cases"
gallery_sat:
  - url: /assets/images/research/mobility/sat_lagos_flood.jpg
    image_path: /assets/images/research/mobility/sat_lagos_flood.jpg
    alt: "Sentinel-1 flood mapping in Lagos, Nigeria"
    title: "Sentinel-1 satellite flood mapping overlaid with POIs in Lagos, Nigeria"
  - url: /assets/images/research/mobility/sat_lagos_framework.jpg
    image_path: /assets/images/research/mobility/sat_lagos_framework.jpg
    alt: "Diagnostic causal-inference framework"
    title: "Satellite + ERA5 + LBS + OpenStreetMap → synthetic DiD causal framework"
gallery_africa:
  - url: /assets/images/research/mobility/africa_sa_pipeline.jpg
    image_path: /assets/images/research/mobility/africa_sa_pipeline.jpg
    alt: "Mobile phone sighting data pipeline for South Africa"
    title: "From raw mobile-phone sightings to province-level mobility metrics"
  - url: /assets/images/research/mobility/africa_sa_mobility.jpg
    image_path: /assets/images/research/mobility/africa_sa_mobility.jpg
    alt: "Inter-regional travel flows in South Africa"
    title: "Inter-regional travel flows during SARS-CoV-2 expansion in South Africa"
---

> **One idea runs through this work:** treat a transportation system as a *differentiable computational graph*, so that classic travel-behavior and traffic-flow theory can be learned directly from big data, while every parameter keeps its physical and economic meaning.

<div class="notice--primary" markdown="1">
**At a glance:** (1) interpretable AI in transportation modeling: computational-graph travel demand learning & economic analysis, interpretable traffic state estimation · (2) emerging data: LBS, climate and health data in the U.S., Nigeria and South Africa · (3) transportation multi-resolution modeling (MRM) & world models.
</div>

## 1. Interpretable AI in Transportation Modeling

Deep learning predicts well but rarely explains. My approach to **interpretable AI** builds the network *from* transportation theory: each layer of a computational graph is a modeling step, and each learned weight is a behavioral, economic or physical parameter. The models train like deep learning, yet every output can be read and explained.

### 1.1 Computational-graph travel demand learning & economic analysis

The classic four-step model (trip generation → distribution → route/line choice → assignment) is rebuilt as a **layered computational graph**. Forward propagation reproduces the model; **backpropagation** calibrates all layers at once against household surveys, mobile-phone data, floating-car data and link counts.

{% include figure_stack id="gallery_cg" caption="(a) **Wu**, Guo, Xian & Zhou (2018), *Transportation Research Part C*; (b) Sun, Guo, **Wu** et al. (2019), *Sensors*." %}

The same graph supports **economic analysis**: each policy is a lever on a node of the graph, and its **marginal effect** on link flows and travel time follows directly from the gradients, e.g., pricing, workplace relocation, population transfer, and mode shift.

{% include figure_stack id="gallery_iml" caption="Sun, Guo, **Wu**, Zhu, Wu, Xian & Zhou (2019), *Sensors*." %}

**Insight:** interpretability comes from *where* theory sits in the graph. Agencies can ask "what if" questions with the same model that fits the data.

- **Wu, X.**, Guo, J., Xian, K., Zhou, X. (2018). Hierarchical travel demand estimation using multiple data sources: A forward and backward propagation algorithmic framework on a layered computational graph. *Transportation Research Part C*, 96, 321–346. [DOI](https://doi.org/10.1016/j.trc.2018.09.021)
- Sun, J., Guo, J., **Wu, X.**, Zhu, Q., Wu, D., Xian, K., Zhou, X. (2019). Analyzing the impact of traffic congestion mitigation: from an explainable neural network learning framework to marginal effect analyses. *Sensors*, 19(10), 2254. [DOI](https://doi.org/10.3390/s19102254)

### 1.2 Interpretable traffic state estimation

Sparse, heterogeneous sensors (loop detectors, probe vehicles, Bluetooth, video) are fused into a continuous space–time traffic state. **Traffic-flow physics**, such as fluid queue models and the calibratable S-shaped three-parameter (S3) traffic stream model, is embedded in the network, so estimates and predictions stay physically meaningful even with missing data.

{% include figure_stack id="gallery_piml" caption="Figures (a)–(b): Lu, Li, **Wu** & Zhou (2023), *TR-C*. Figures (c)–(d): Shao, Shao, **Wu**, Cheng & Lam (2025), *TR-C*." %}

**Insight:** the physics layer recovers congestion shockwaves that pure data smoothing misses, and keeps predicted speed–flow pairs on a calibrated fundamental diagram.

- Shao, F., Shao, H., **Wu, X.**, Cheng, Q., Lam, W.H.K. (2025). A physics-informed machine learning framework for speed-flow prediction: Integrating an S-shaped traffic stream model with deep learning models. *Transportation Research Part C*, 180, 105362. [DOI](https://doi.org/10.1016/j.trc.2025.105362)
- Lu, J., Li, C., **Wu, X.**, Zhou, X.S. (2023). Physics-informed neural networks for integrated traffic state and queue profile estimation: A differentiable programming approach on layered computational graphs. *Transportation Research Part C*, 153, 104224. [DOI](https://doi.org/10.1016/j.trc.2023.104224)

## 2. Emerging Data: LBS, Climate & Health {#emerging-data}

With the Villanova team, I combine **location-based service (LBS) data, climate and satellite data, and public-health data** to measure how people move during disasters and epidemics, in the U.S. Gulf Coast, Lagos (Nigeria) and South Africa.

### 2.1 LBS data: human mobility during extreme events
{% include figure_stack id="gallery_lbs" caption="Two-stage model: hurricane → mobility → COVID-19 (Liu, **Wu** et al., 2025, *Journal of Transport Geography*)." %}

### 2.2 Climate data: satellite flood mapping and precipitation
{% include figure_stack id="gallery_sat" caption="Sentinel-1 flood extents, ERA5 precipitation and device-level POI visits feed a synthetic difference-in-differences estimator (Zhang, **Wu** et al., 2026, *IJDRR*)." %}

### 2.3 Health data: mobility and SARS-CoV-2 transmission
{% include figure_stack id="gallery_africa" caption="Mobile-phone mobility metrics and structural equation modeling across South African provinces (Luo, **Wu** et al., 2025, *PLOS ONE*)." %}

**Insight:** mobility is the missing link between hazards and health outcomes. Shifting the unit of analysis (e.g., from places to facility types) makes causal inference possible even when no unaffected control region exists.

- Liu, K., **Wu, X.**, Molnar, L., Hu, S., Zhang, L., Xiong, C. (2025). Characterizing human mobility and its impact on the spread of COVID-19 during extreme weather events: A case study of hurricane Laura. *Journal of Transport Geography*, 129, 104423. [DOI](https://doi.org/10.1016/j.jtrangeo.2025.104423)
- Liu, K., **Wu, X.**, Zhang, L., Xiong, C. (2024). Characterize human mobility in Nigeria during flooding season and its impact in shaping the spread of COVID-19. *IEEE GHTC 2024*, 56–63. [DOI](https://doi.org/10.1109/GHTC62424.2024.10771507)
- Zhang, L., **Wu, X.**, Liu, K., Al Mehedi, M.A., Zhou, J., Smith, V., Xiong, C. (2026). Diagnostic framework for causal inference in seasonal urban flooding: Precipitation-based control selection and synthetic difference-in-differences in Lagos, Nigeria. *International Journal of Disaster Risk Reduction*, 105993. [DOI](https://doi.org/10.1016/j.ijdrr.2026.105993)
- Zhang, L., **Wu, X.**, Liu, K., Xiong, C. (2024). Evaluating the spatial-temporal impact of urban flooding on mobility patterns and point of interest. *IEEE GHTC 2024*, 424–430. [DOI](https://doi.org/10.1109/GHTC62424.2024.10771563)
- Luo, W., **Wu, X.**, Li, R., Fitzpatrick, M., Charurat, M., Blanco, N., et al., Xiong, C. (2025). Variant patterns and influence of inter-regional travel during the SARS-CoV-2 expansion in South Africa. *PLOS ONE*, 20(11), e0329621. [DOI](https://doi.org/10.1371/journal.pone.0329621)

<div class="notice--info" markdown="1">
**INFORM Africa (NIH):** this work is part of the NIH-funded *INFORM Africa* research hub (Project 2: human mobility and infectious disease dynamics), where I serve as project manager and co-developed an open training package for African researchers. See [Teaching & Training]({{ "/teaching/" | relative_url }}#inform-africa).
</div>

## 3. Transportation Multi-Resolution Modeling (MRM) & World Models

Planning models (macro), dynamic traffic assignment (meso) and queue dynamics (micro) are connected through **queue-based performance functions**. The inflow demand-to-capacity ratio drives congestion duration, speed drop and delay, bridging the polynomial arrival queue model and volume-delay functions. This line also covers my work on traffic assignment and dynamic traffic assignment for FHWA, ADOT, MAG and NVTA.

{% include figure_stack id="gallery_mrm" caption="Meso-to-macro cross-resolution approach (Zhou, Cheng, **Wu** et al., 2022, *Multimodal Transportation*, **2022 Best Article Award**) and queue-based V/C calibration (**Wu** et al., TRB 2021, cited by an FHWA handbook)." %}

**Insight:** a queue-based V/C ratio gives capacity estimates that stay consistent across resolutions, so one calibrated network can serve regional planning models (FHWA, ADOT, MAG) as well as dynamic traffic assignment.

- Zhou, X.S., Cheng, Q., **Wu, X.** (corresponding), Li, P., Belezamo, B., Lu, J., Abbasi, M. (2022). A meso-to-macro cross-resolution performance approach for connecting polynomial arrival queue model to volume-delay function with inflow demand-to-capacity ratio. *Multimodal Transportation*, 1(2), 100017. [DOI](https://doi.org/10.1016/j.multra.2022.100017)
- **Wu, X.**, Dutta, A., Zhang, W., Zhu, H., Livshits, V., Zhou, X.S. (2021). Characterization and calibration of volume-to-capacity ratio in volume-delay functions on freeways based on a queue analysis approach. *Proceedings of the 100th TRB Annual Meeting*, Washington, D.C.
- Cheng, Q., Liu, Z., Guo, J., **Wu, X.**, Pendyala, R., Belezamo, B., Zhou, X.S. (2022). Estimating key traffic state parameters through parsimonious spatial queue models. *Transportation Research Part C*, 137, 103596. [DOI](https://doi.org/10.1016/j.trc.2022.103596)
- Belezamo, B., **Wu, X.**, Avcı, C., Zhou, X. (2019). Kinematic wave-oriented Markov chain model to capture the spatiotemporal correlations of coupled traffic states. *IEEE ITSC 2019*, 2343–2348.
- Zhuge, L., Li, W., Guo, J., Xian, K., **Wu, X.**, Zhou, X. (2018). A tree-based reoptimization framework for solving traffic assignment problem in rapid decision making applications. *CICTP 2018*, 205–214.


---
*Figures are reproduced from the author's own publications for scholarly, non-commercial illustration; please cite the original articles.*
