---
layout: single
title: "Supply Chain & Logistics Optimization"
permalink: /supply-chain-logistics/
author_profile: true
toc: true
toc_sticky: true
toc_label: "Research Threads"
excerpt: "Supply chain research: perishable supply chains and multi-echelon location, synchronized service network design and decomposition algorithms, and service design with QFD."
header:
  overlay_image: /assets/images/research/banner_logistics.jpg
  overlay_filter: 0.5
  caption: "Profit surfaces of a perishable food supply chain under a variational inequality model (Wu et al., 2018, TR-E)"
gallery_qap:
  - image_path: /assets/images/research/logistics/qap_timespace.jpg
    title: "(a) Time-expanded service network and its network-based QAP (NET-QAP) representation"
  - image_path: /assets/images/research/logistics/qap_network.jpg
    title: "(b) Inbound and outbound timeslots linked by transshipment edges"
  - image_path: /assets/images/research/logistics/qap_bnb.jpg
    title: "(c) Branch-and-bound search guided by the Extended Gilmore–Lawler Bound (EGLB)"
  - image_path: /assets/images/research/logistics/qap_jd_network.jpg
    title: "(d) JD Logistics e-commerce case: physical network of 16 warehouses, 12 distribution centers and 20 pick-up stations"
gallery_lot:
  - image_path: /assets/images/research/logistics/lotsizing_decisions.jpg
    title: "(a) Three decisions: where to produce, which DC serves which train, and how much to replenish on board"
  - image_path: /assets/images/research/logistics/lotsizing_flows.jpg
    title: "(b) Lot-sizing flows without vs. with in-station pedestrian congestion"
  - image_path: /assets/images/research/logistics/lotsizing_congestion_costs.jpg
    title: "(c) Ignoring in-station congestion misstates set-up, transportation and storage costs, revenue and profit"
gallery_catering:
  - image_path: /assets/images/research/logistics/catering_network_timetable.jpg
    title: "(a) Food suppliers, DCs and rail stations on an HSR network, linked to the train timetable"
  - image_path: /assets/images/research/logistics/catering_routes.jpg
    title: "(b) Location-routing: routes of refrigerated cars from DCs to trains on the operational network"
  - image_path: /assets/images/research/logistics/catering_rc_schedule.jpg
    title: "(c) Optimized routes and time schedules of each refrigerated car, with capacity utilization"
gallery_pfsc:
  - image_path: /assets/images/research/logistics/pfsc_chain.jpg
    title: "(a) Perishable food supply chain: suppliers → regional DCs → rail stations → high-speed trains"
  - image_path: /assets/images/research/logistics/pfsc_vi_surface.jpg
    title: "(b) Equilibrium profit surfaces under different arc multipliers, costs and selling prices"
gallery_qfd:
  - image_path: /assets/images/research/logistics/qfd_house_of_quality.jpg
    title: "(a) Two-phase fuzzy QFD: quality deployment and functional deployment \"houses of quality\" linking basic requirements, assessment criteria and service stations"
  - image_path: /assets/images/research/logistics/qfd_bodies_of_evidence.jpg
    title: "(b) Expert judgments as bodies of evidence (consonant, nested, mixed) and their fuzzy importance ratings"
  - image_path: /assets/images/research/logistics/qfd_belief_plausibility.jpg
    title: "(c) Belief and plausibility measures of evidence for crisp and fuzzy sets"
  - image_path: /assets/images/research/logistics/qfd_reasoning.jpg
    title: "(d) Evidence-based approximate reasoning: rules combine facts into the conclusion for each service station"
---

> **Goal:** design supply chains and logistics services that are *on time, synchronized and solvable at real-world scale*, by pairing rigorous formulations (VI, QAP, MINLP) with decomposition algorithms that exploit network structure.

<div class="notice--primary" markdown="1">
**At a glance:** (1) perishable supply chains and multi-echelon distribution location · (2) synchronized service network design and large-scale decomposition algorithms · (3) service design with robust fuzzy QFD. *Click any figure to enlarge it.*
</div>

## 1. Supply Chain

### 1.1 Perishable supply chains & multi-echelon distribution location

Every day, meals must move from suppliers to distribution centers (DCs), to rail stations, and onto **thousands of trains with tight time windows and deadlines**. A **three-echelon location-routing model** chooses DC locations and builds refrigerated-car routes directly from the train timetable.

{% include figure_stack id="gallery_catering" caption="**Wu**, Nie & Xu (2017), *Transportation Research Part C*." %}

<figure class="figure-stack figure-stack--small">
  <a href="{{ '/assets/images/research/logistics/catering_network_map.jpg' | relative_url }}" class="image-popup" title="Candidate DCs and rail stations along the Beijing–Shanghai high-speed line"><img src="{{ '/assets/images/research/logistics/catering_network_map.jpg' | relative_url }}" alt="Candidate DCs and rail stations along the Beijing–Shanghai high-speed line"></a>
  <figcaption>Real-world case: candidate DCs and rail stations along the Beijing–Shanghai high-speed line.</figcaption>
</figure>

A **variational inequality (VI)** model captures the equilibrium of a perishable food supply chain with **uncertain on-train demand** (newsvendor) and **path time-deadline constraints** under flow-dependent lead times. Deadlines are reformulated with the Dirac delta function so they can be dualized, and the model is solved by an **Euler algorithm with an augmented Lagrangian dual**. The case study covers 246 trains on the Beijing–Shanghai corridor.

{% include figure_stack id="gallery_pfsc" caption="**Wu**, Nie, Xu & Yan (2018), *Transportation Research Part E*." %}

**Insight:** freshness is a *path* constraint, not an arc constraint. Writing it in VI form shows how deadlines reshape equilibrium flows and profits.

- **Wu, X.**, Nie, L., Xu, M., Yan, F. (2018). A perishable food supply chain problem considering demand uncertainty and time deadline constraints: Modeling and application to a high-speed railway catering service. *Transportation Research Part E*, 111, 186–209. [DOI](https://doi.org/10.1016/j.tre.2018.01.002)
- **Wu, X.**, Nie, L., Xu, M. (2017). Designing an integrated distribution system for catering services for high-speed railways: A three-echelon location routing model with tight time windows and time deadlines. *Transportation Research Part C*, 74, 212–244. [DOI](https://doi.org/10.1016/j.trc.2016.11.006)
- Jiang, Y., **Wu, X.**, Chen, Y. (2020). Designing a flexible catering system for high-speed railway considering departure time selection and time deadline constraints. *IEEE Access*, 8, 44300–44317. [DOI](https://doi.org/10.1109/ACCESS.2020.2978180)

### 1.2 Synchronized service network design & decomposition algorithms

In a transshipment hub, **inbound and outbound services must be scheduled together** so that goods are sorted and forwarded without long waits. I developed a **network-based QAP (NET-QAP)** that linearizes the classic Koopmans–Beckmann QAP and generalizes it, then solves it with an **Extended Gilmore–Lawler Bound (EGLB)** inside branch-and-bound.

This work was done **with JD Logistics (Jingdong)**, and it is tested on two industry settings: a **rail-to-truck transshipment terminal**, and an **e-commerce "second-wave" delivery network** with 16 warehouses, 20 pick-up stations and 12 distribution centers, where orders placed before the afternoon cutoff are delivered by the next morning.

{% include figure_stack id="gallery_qap" caption="**Wu**, Lu, Wu & Zhou (2021), *Transportation Research Part B*." %}

**Insight:** viewing synchronization as an *assignment of services to timeslots* turns a hard scheduling problem into a QAP with a network structure, and that structure yields tight bounds and an efficient exact search.

Where should each food product be produced, which DC should serve which train, and how much should be replenished at each stop, when **pedestrian congestion** in stations slows handling? A nonlinear MIP on a lot-sizing network is decomposed by **Lagrangian substitution** into a MILP and a sequence of univariate concave problems.

{% include figure_stack id="gallery_lot" caption="**Wu**, Nie, Xu & Zhao (2019), *Transportation Research Part E*." %}

- **Wu, X.**, Lu, J., Wu, S., Zhou, X.S. (2021). Synchronizing time-dependent transportation services: Reformulation and solution algorithm using quadratic assignment problem. *Transportation Research Part B*, 152, 140–179. [DOI](https://doi.org/10.1016/j.trb.2021.08.008)
- **Wu, X.**, Nie, L., Xu, M., Zhao, L. (2019). Distribution planning problem for a high-speed rail catering service considering time-varying demands and pedestrian congestion: A lot-sizing-based model and decomposition algorithm. *Transportation Research Part E*, 123, 61–89. [DOI](https://doi.org/10.1016/j.tre.2019.01.003)
- Jiang, Y., He, T., Xiong, J., **Wu, X.**, Chen, Y. (2020). Parallel machine production and transportation operations' scheduling with tight time windows. *Complexity*, 2020, 1381340. [DOI](https://doi.org/10.1155/2020/1381340)

### 1.3 Service design & quality function deployment (QFD)

For **service design**, such as choosing service stations and DC locations, customer requirements are translated into technical decisions under **fuzziness and randomness**, using a two-phase fuzzy QFD that combines **evidence theory** with fuzzy sets, and a robust fuzzy QFD based on the mean-end-chain concept.

{% include figure_stack id="gallery_qfd" caption="**Wu**, Nie & Xu (2015), *Mathematical Problems in Engineering*; extended in **Wu**, Nie & Xu (2017), *European Journal of Operational Research*." %}

- **Wu, X.**, Nie, L., Xu, M. (2017). Robust fuzzy quality function deployment based on the mean-end-chain concept: Service station evaluation problem for rail catering services. *European Journal of Operational Research*, 263(3), 974–995. [DOI](https://doi.org/10.1016/j.ejor.2017.05.036)
- **Wu, X.**, Nie, L., Xu, M. (2015). Service station evaluation problem in catering service of the high-speed railway: a fuzzy QFD approach based on evidence theory. *Mathematical Problems in Engineering*, 2015, 404926. [DOI](https://doi.org/10.1155/2015/404926)
- **Wu, X.**, Nie, L., Xu, M., Fu, H. (2016). Fuzzy QFD for distribution center location evaluation in catering service of high-speed railway. *Management & Engineering*, 22, 83.

---
*Figures are reproduced from the author's own publications for scholarly, non-commercial illustration; please cite the original articles.*
