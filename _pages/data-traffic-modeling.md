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
  overlay_filter: "linear-gradient(120deg, rgba(19, 39, 74, 0.80), rgba(44, 102, 176, 0.35))"
  caption: "Network-wide speed–flow prediction errors on Los Angeles freeways (Shao et al., 2025, TR-C)"
gallery_cases:
  - image_path: /assets/images/research/mobility/piml_la_map.jpg
    title: "Los Angeles, CA: network-wide speed–flow prediction on 150 Caltrans District 7 freeway sensors (physics-informed computational graph)"
  - image_path: /assets/images/research/mobility/cg_policy_beijing.jpg
    title: "Beijing, China: travel demand, path flows and link flows on a subnetwork with 2,502 nodes, 5,397 links, 236 zones and 14,967 OD pairs"
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
gallery_mtcg:
  - image_path: /assets/images/research/mobility/mtcg_melbourne_network.jpg
    title: "Melbourne, Australia: 2,077 nodes, 4,223 links, 416 centroids and 24,160 OD pairs"
  - image_path: /assets/images/research/mobility/mtcg_melbourne_events.jpg
    title: "Melbourne: link-flow error reduction and flow changes on stadium-event days vs. regular days"
gallery_phoenix:
  - image_path: /assets/images/research/mobility/mrm_maricopa_network.jpg
    title: "Phoenix metropolitan region (MAG travel demand model network: 21,945 nodes, 52,846 directional links): observed link volume and speed profile"
  - image_path: /assets/images/research/mobility/mrm_vc_calibration.jpg
    title: "Queue-based (QBM) vs. density-based (DBM) and volume-based (VBM) estimates of period capacity on Phoenix freeways"
  - image_path: /assets/images/research/mobility/mrm_phoenix_i10_corridor.jpg
    title: "Phoenix I-10 freeway corridor and its four loop detectors (137, 78, 84, 139)"
  - image_path: /assets/images/research/mobility/mrm_cumulative_queue.jpg
    title: "Queue-based view of a bottleneck: arrival rate above capacity builds a queue; cumulative arrival and discharge curves give the queue length, waiting time and total delay (shaded)"
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
gallery_mrm:
  - image_path: /assets/images/research/mobility/mrm_speed_arrival.jpg
    title: "(a) During congestion (t0 to t3), speed drops below the cut-off speed while the arrival rate exceeds the discharge rate"
  - image_path: /assets/images/research/mobility/mrm_virtual_queue.jpg
    title: "(b) Virtual queue at the bottleneck vs. the physical spatial queue along the road"
  - image_path: /assets/images/research/mobility/mrm_trajectories.jpg
    title: "(c) Mesoscopic vehicle trajectories through the bottleneck: travel time = free-flow time + queue waiting time w(t)"
  - image_path: /assets/images/research/mobility/mrm_i405.jpg
    title: "(d) Los Angeles I-405 Northbound bottleneck: observed space–time congestion"
gallery_lbs:
  - image_path: /assets/images/research/mobility/lbs_hurricane_laura.jpg
    title: "U.S. Gulf Coast (Louisiana, Texas, Arkansas, Mississippi): Hurricane Laura track and affected counties, August 26–27, 2020"
  - image_path: /assets/images/research/mobility/lbs_evacuation_orders.jpg
    title: "Louisiana and Texas: county-level mandatory and voluntary evacuation orders with issue dates"
  - image_path: /assets/images/research/mobility/lbs_laura_results.jpg
    title: "Louisiana and Texas: estimated change in new COVID-19 cases from hurricane- and evacuation-driven mobility"
gallery_sat:
  - image_path: /assets/images/research/mobility/sat_lagos_nigeria.jpg
    title: "Nigeria: location of the Lagos State study area (orange)"
  - image_path: /assets/images/research/mobility/sat_lagos_flood.jpg
    title: "Lagos State, Nigeria: Sentinel-1 satellite flood extents, permanent water, urban area and POIs across the 2020 rainy season"
  - image_path: /assets/images/research/mobility/climate_nigeria_floods.jpg
    title: "Nigeria (all local government areas, LGAs): flooded area per LGA, May 16–31, 2020"
  - image_path: /assets/images/research/mobility/sat_lagos_framework.jpg
    title: "Lagos: Sentinel-1 imagery + ERA5 precipitation + LBS POI visits + OpenStreetMap feed a synthetic difference-in-differences causal framework"
gallery_lagos_abm:
  - image_path: /assets/images/research/mobility/lagos_lbs_sightings.jpg
    title: "Lagos State, Nigeria: raw location-based-service sightings, January–October 2020 (6.67 billion sightings → about 13 million OD trips)"
  - image_path: /assets/images/research/mobility/lagos_infection_hotspots.jpg
    title: "Lagos State, Nigeria: estimated COVID-19 infections by geohash cell on June 1, 2020 (5,367 cells across 20 LGAs)"
gallery_africa:
  - image_path: /assets/images/research/mobility/africa_sa_mobility.jpg
    title: "South Africa (9 provinces, 52 districts): three types of inter-regional travel flows from mobile-phone data during SARS-CoV-2 expansion"
  - image_path: /assets/images/research/mobility/africa_sa_pipeline.jpg
    title: "South Africa: from raw mobile-phone sightings to province-level mobility metrics and a structural equation model of daily COVID-19 cases"
---

> **One idea runs through this work:** treat a transportation system as a *differentiable computational graph*, so that classic travel-behavior and traffic-flow theory can be learned directly from big data, while every parameter keeps its physical and economic meaning.

<div class="notice--primary" markdown="1">
**At a glance:** (1) interpretable AI in transportation modeling: computational-graph travel demand learning & economic analysis, interpretable traffic state estimation · (2) emerging data: LBS, climate and health data in the U.S., Nigeria and South Africa · (3) transportation multi-resolution modeling (MRM) & world models.
</div>

## Real-World Case Studies at Scale

| City / region | Network and data | Scale | Papers |
|---|---|---|---|
| **Los Angeles**, CA | Caltrans District 7 freeway sensors (PeMS); I-405 bottleneck | 150 sensors network-wide; 22 detectors on a 6-mile corridor, 4 months | Shao, Wu et al. 2025 *TR-C*; Zhou et al. 2022; Cheng et al. 2022 |
| **Beijing**, China | Regional travel demand subnetwork (Beijing Transport Institute data); West 3rd Ring Road freeway bottleneck | 2,502 nodes · 5,397 links · 236 zones · 14,967 OD pairs · 40,494 paths | Wu et al. 2018 *TR-C*; Sun et al. 2019 *Sensors*; Cheng et al. 2022 *TR-C* |
| **Phoenix** (Maricopa County), AZ | MAG regional travel demand model; ADOT freeway detectors on I-10 | 21,945 nodes · 52,846 directional links; I-10 corridor, 365 days of 2016 | Wu et al. 2021 *TRB*; Belezamo, Wu et al. 2019 *IEEE ITSC*; Zhou, Cheng, Wu et al. 2022 *Multimodal Transportation* |
| **Melbourne**, Australia | Large urban network with regular, POI and stadium-event days | 2,077 nodes · 4,223 links · 416 centroids · 24,160 OD pairs | Shao, Wu et al. (under review, 2026) |
| **Lagos State**, Nigeria | Mobile-device LBS sightings, Sentinel-1 flood imagery, serology data | 6.67 billion sightings → about 13 million OD trips; 5,367 geohash cells across 20 LGAs | Zhang et al. 2026 *IJDRR*; Liu, Wu et al. (under review, 2026) |
| **New York**, NY | Midtown Manhattan – JFK Airport corridor | Freeway bottleneck queue analysis | Cheng et al. 2022 *TR-C* |
| **Louisiana & Texas** (U.S. Gulf Coast) | Hurricane Laura (2020): mobile-device LBS data, evacuation orders, COVID-19 cases | County-level daily panel across the affected region | Liu, Wu et al. 2025 *JTG* |
| **South Africa** | Inter-regional travel and SARS-CoV-2 variants: mobile-phone sightings | 9 provinces · 52 districts | Luo, Wu et al. 2025 *PLOS ONE* |
| **7 African countries** | Mobility and non-communicable diseases (diabetes, CVD): ongoing NIH pilot | Nigeria, South Africa, Ghana, Botswana, Gabon, Congo, Ethiopia | Ongoing |

## 1. Interpretable AI in Transportation Modeling

Deep learning predicts well but rarely explains. My approach to **interpretable AI** builds the network *from* transportation theory: each layer of a computational graph is a modeling step, and each learned weight is a behavioral, economic or physical parameter. The models train like deep learning, yet every output can be read and explained.

{% include figure_stack id="gallery_cases" caption="Shao, Shao, **Wu**, Cheng & Lam (2025), *TR-C*; Sun, Guo, **Wu** et al. (2019), *Sensors*." %}

### 1.1 Computational-graph travel demand learning & economic analysis

The classic four-step model (trip generation → distribution → route/line choice → assignment) is rebuilt as a **layered computational graph**. Forward propagation reproduces the model; **backpropagation** calibrates all layers at once against household surveys, mobile-phone data, floating-car data and link counts.

{% include figure_stack id="gallery_cg" caption="(a) **Wu**, Guo, Xian & Zhou (2018), *Transportation Research Part C*; (b) Sun, Guo, **Wu** et al. (2019), *Sensors*." %}

The same graph supports **economic analysis**: each policy is a lever on a node of the graph, and its **marginal effect** on link flows and travel time follows directly from the gradients, e.g., pricing, workplace relocation, population transfer, and mode shift.

{% include figure_stack id="gallery_iml" caption="Sun, Guo, **Wu**, Zhu, Wu, Xian & Zhou (2019), *Sensors*." %}

**New (under review): Melbourne, Australia.** Daily traffic mixes regular commuting, major events and tourist attractions. A computational-graph model learns these contexts from data on the full Melbourne network, including days with POI activities and stadium events, and recovers the value of time within 3% of its benchmark.

{% include figure_stack id="gallery_mtcg" caption="Shao, **Wu** (corresponding), Zhao, Shao & Lam, manuscript under review (2026)." %}

**Insight:** interpretability comes from *where* theory sits in the graph. Agencies can ask "what if" questions with the same model that fits the data.

- **Wu, X.**, Guo, J., Xian, K., Zhou, X. (2018). Hierarchical travel demand estimation using multiple data sources: A forward and backward propagation algorithmic framework on a layered computational graph. *Transportation Research Part C*, 96, 321–346. [DOI](https://doi.org/10.1016/j.trc.2018.09.021)
- Sun, J., Guo, J., **Wu, X.** (corresponding), Zhu, Q., Wu, D., Xian, K., Zhou, X. (2019). Analyzing the impact of traffic congestion mitigation: from an explainable neural network learning framework to marginal effect analyses. *Sensors*, 19(10), 2254. [DOI](https://doi.org/10.3390/s19102254)

### 1.2 Computational-graph-based interpretable traffic state estimation

Sparse, heterogeneous sensors (loop detectors, probe vehicles, Bluetooth, video) are fused into a continuous space–time traffic state. **Traffic-flow physics**, such as fluid queue models and the calibratable S-shaped three-parameter (S3) traffic stream model, is embedded in the network, so estimates and predictions stay physically meaningful even with missing data.

{% include figure_stack id="gallery_piml" caption="Lu, Li, **Wu** & Zhou (2023), *TR-C*; Shao, Shao, **Wu**, Cheng & Lam (2025), *TR-C*." %}

**Insight:** the physics layer recovers congestion shockwaves that pure data smoothing misses, and keeps predicted speed–flow pairs on a calibrated fundamental diagram.

- Shao, F., Shao, H., **Wu, X.** (corresponding), Cheng, Q., Lam, W.H.K. (2025). A physics-informed machine learning framework for speed-flow prediction: Integrating an S-shaped traffic stream model with deep learning models. *Transportation Research Part C*, 180, 105362. [DOI](https://doi.org/10.1016/j.trc.2025.105362)
- Lu, J., Li, C., **Wu, X.**, Zhou, X.S. (2023). Physics-informed neural networks for integrated traffic state and queue profile estimation: A differentiable programming approach on layered computational graphs. *Transportation Research Part C*, 153, 104224. [DOI](https://doi.org/10.1016/j.trc.2023.104224)

## 2. Emerging Data: LBS, Climate & Health {#emerging-data}

With the Villanova team, I combine **location-based service (LBS) data, climate and satellite data, and public-health data** to measure how people move during disasters and epidemics, in the U.S. Gulf Coast, Lagos (Nigeria) and South Africa.

### 2.1 LBS data: human mobility during extreme events
**Field case: U.S. Gulf Coast, Hurricane Laura (2020).** Mobile-device location data for counties in Louisiana and Texas show how the hurricane and evacuation orders changed trips, and how those trips shaped COVID-19 spread.

{% include figure_stack id="gallery_lbs" caption="Liu, **Wu**, Molnar, Hu, Zhang & Xiong (2025), *Journal of Transport Geography*." %}

**Map-matching volatile LBS trajectories.** Raw LBS points are sparse and noisy, so they must be snapped to the road network before trips can be measured. Sup-HMM, a Bayesian-optimized hidden Markov model, keeps map-matching accurate on volatile trajectories (Li, **Wu** et al. 2026, *IEEE Transactions on Intelligent Transportation Systems*, co-first author; [DOI](https://doi.org/10.1109/TITS.2026.3740031)).

### 2.2 Climate data: satellite flood mapping and precipitation
**Field cases: Lagos State and Nigeria (2020 rainy season).** Sentinel-1 satellite imagery and ERA5 precipitation locate floods; LBS data on visits to points of interest measure how people responded, from Lagos neighborhoods to all of Nigeria.

{% include figure_stack id="gallery_sat" caption="Zhang, **Wu** et al. (2026), *International Journal of Disaster Risk Reduction*; Liu, **Wu** et al. (2024), *IEEE GHTC*." %}

### 2.3 Health data: mobility and SARS-CoV-2 transmission (South Africa and Lagos)
**Field case: South Africa (all 9 provinces).** Panel mobile-phone sighting data reveal how inter-regional travel shaped the spread of SARS-CoV-2 variants.

{% include figure_stack id="gallery_africa" caption="Luo, **Wu** et al. (2025), *PLOS ONE*, INFORM Africa research hub." %}

**Field case: Lagos State, Nigeria (2020, under review).** Billions of mobile-device sightings are turned into city-wide daily mobility for the population of Lagos State and linked with serology data to estimate how mobility restrictions changed COVID-19 spread.

{% include figure_stack id="gallery_lagos_abm" caption="Liu, **Wu** (co-first author), Xiong et al., manuscript under review (2026), INFORM Africa research hub." %}

**Ongoing pilot: mobility and non-communicable diseases across 7 African countries.** Can mobile-phone mobility tell us about chronic disease risk? Mobility metrics (walking share, driving share, trips per day, distance from home, night trips) are compared with 2019 incidence of diabetes, cardiovascular disease, stroke and chronic respiratory disease in Nigeria, South Africa, Ghana, Botswana, Gabon, Congo and Ethiopia.

<figure class="figure-stack">
  <a href="{{ '/assets/images/research/mobility/health_ncd_mobility.jpg' | relative_url }}" class="image-popup" title="Mobility metrics vs. disease incidence across 7 African countries"><img src="{{ '/assets/images/research/mobility/health_ncd_mobility.jpg' | relative_url }}" alt="Spearman correlations between mobility metrics and disease incidence, including diabetes"></a>
  <figcaption>7 African countries (Nigeria, South Africa, Ghana, Botswana, Gabon, Congo, Ethiopia): Spearman correlations between mobile-phone mobility metrics (2020–21) and IHME 2019 incidence of diabetes, cardiovascular disease, stroke and chronic respiratory disease. Ongoing NIH pilot study.</figcaption>
</figure>

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

**Phoenix case: regional network and freeway corridor.** For the Maricopa Association of Governments (MAG), I calibrated queue-based V/C ratios across the full regional network, and on the ADOT I-10 corridor, cumulative arrival and discharge curves turn detector counts into queue length, delay and congestion duration.

{% include figure_stack id="gallery_phoenix" caption="Regional network and V/C calibration: **Wu**, Dutta, Zhang, Zhu, Livshits & Zhou (2021), TRB Annual Meeting. I-10 corridor and cumulative-curve queue model: Zhou, Cheng, **Wu** (corresponding) et al. (2022), *Multimodal Transportation*." %}

<figure class="figure-stack figure-stack--small mrm-steps">
  <a href="{{ '/assets/images/research/mobility/mrm_qvdf_steps.jpg' | relative_url }}" class="image-popup" title="Steps from inflow demand to link performance"><img src="{{ '/assets/images/research/mobility/mrm_qvdf_steps.jpg' | relative_url }}" alt="Steps of the queue-based volume-delay function"></a>
  <figcaption>From inflow demand to link performance: demand-to-capacity ratio → congestion duration → queued delay and speed reduction → time-dependent queue → macro (average) and meso (time-dependent) performance.</figcaption>
</figure>

{% include figure_stack id="gallery_mrm" caption="Meso-to-macro cross-resolution approach (Zhou, Cheng, **Wu** et al., 2022, *Multimodal Transportation*, **2022 Best Article Award**) and queue-based V/C calibration (**Wu** et al., TRB 2021, cited by an FHWA handbook)." %}

**Insight:** a queue-based V/C ratio gives capacity estimates that stay consistent across resolutions, so one calibrated network can serve regional planning models (FHWA, ADOT, MAG) as well as dynamic traffic assignment.

- Zhou, X.S., Cheng, Q., **Wu, X.** (corresponding), Li, P., Belezamo, B., Lu, J., Abbasi, M. (2022). A meso-to-macro cross-resolution performance approach for connecting polynomial arrival queue model to volume-delay function with inflow demand-to-capacity ratio. *Multimodal Transportation*, 1(2), 100017. [DOI](https://doi.org/10.1016/j.multra.2022.100017)
- **Wu, X.**, Dutta, A., Zhang, W., Zhu, H., Livshits, V., Zhou, X.S. (2021). Characterization and calibration of volume-to-capacity ratio in volume-delay functions on freeways based on a queue analysis approach. *Proceedings of the 100th TRB Annual Meeting*, Washington, D.C.
- Cheng, Q., Liu, Z., Guo, J., **Wu, X.**, Pendyala, R., Belezamo, B., Zhou, X.S. (2022). Estimating key traffic state parameters through parsimonious spatial queue models. *Transportation Research Part C*, 137, 103596. [DOI](https://doi.org/10.1016/j.trc.2022.103596)
- Belezamo, B., **Wu, X.** (corresponding), Avcı, C., Zhou, X. (2019). Kinematic wave-oriented Markov chain model to capture the spatiotemporal correlations of coupled traffic states. *IEEE ITSC 2019*, 2343–2348.
- Zhuge, L., Li, W., Guo, J., Xian, K., **Wu, X.**, Zhou, X. (2018). A tree-based reoptimization framework for solving traffic assignment problem in rapid decision making applications. *CICTP 2018*, 205–214.


---
*Figures are reproduced from the author's own publications for scholarly, non-commercial illustration; please cite the original articles.*
