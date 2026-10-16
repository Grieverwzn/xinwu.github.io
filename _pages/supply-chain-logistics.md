---
layout: single
title: "Supply Chain & Logistics Optimization"
permalink: /supply-chain-logistics/
author_profile: true
toc: true
toc_sticky: true
toc_label: "Research Threads"
excerpt: "Supply chain research: synchronized service network design and decomposition algorithms, perishable supply chains and multi-echelon location, and service design with QFD."
header:
  overlay_image: /assets/images/research/banner_logistics.jpg
  overlay_filter: 0.5
  caption: "Profit surfaces of a perishable food supply chain under a variational inequality model (Wu et al., 2018, TR-E)"
gallery_catering:
  - url: /assets/images/research/logistics/catering_chain.jpg
    image_path: /assets/images/research/logistics/catering_chain.jpg
    alt: "Three-echelon HSR catering distribution system"
    title: "Food suppliers → distribution centers → rail stations → trains"
  - url: /assets/images/research/logistics/catering_pdn.jpg
    image_path: /assets/images/research/logistics/catering_pdn.jpg
    alt: "Physical distribution network built from the train timetable"
    title: "Turning a train timetable into a physical distribution network"
gallery_pfsc:
  - url: /assets/images/research/logistics/pfsc_chain.jpg
    image_path: /assets/images/research/logistics/pfsc_chain.jpg
    alt: "Perishable food supply chain for HSR catering"
    title: "Perishable food supply chain for HSR catering services"
  - url: /assets/images/research/logistics/pfsc_vi_surface.jpg
    image_path: /assets/images/research/logistics/pfsc_vi_surface.jpg
    alt: "Total profit surfaces under different parameters"
    title: "Equilibrium profit surfaces under different arc multipliers, costs and prices"
gallery_lot:
  - url: /assets/images/research/logistics/lotsizing_decisions.jpg
    image_path: /assets/images/research/logistics/lotsizing_decisions.jpg
    alt: "Three decisions of the distribution plan"
    title: "Where to produce, which DC serves which train, and how to replenish on board"
  - url: /assets/images/research/logistics/lotsizing_flows.jpg
    image_path: /assets/images/research/logistics/lotsizing_flows.jpg
    alt: "Flow patterns on the lot-sizing network"
    title: "Lot-sizing flows without vs. with in-station pedestrian congestion"
  - url: /assets/images/research/logistics/lotsizing_lagrangian.jpg
    image_path: /assets/images/research/logistics/lotsizing_lagrangian.jpg
    alt: "Lagrangian decomposition procedure"
    title: "Lagrangian substitution: MILP + univariate concave subproblems"
gallery_qap:
  - url: /assets/images/research/logistics/qap_timespace.jpg
    image_path: /assets/images/research/logistics/qap_timespace.jpg
    alt: "Time-expanded network and QAP network representation"
    title: "Time-expanded service network ↔ network-based QAP representation"
  - url: /assets/images/research/logistics/qap_network.jpg
    image_path: /assets/images/research/logistics/qap_network.jpg
    alt: "Inbound and outbound timeslots with transshipment edges"
    title: "Inbound/outbound timeslots linked by transshipment edges"
  - url: /assets/images/research/logistics/qap_bnb.jpg
    image_path: /assets/images/research/logistics/qap_bnb.jpg
    alt: "Branch-and-bound tree with EGLB lower bounds"
    title: "Branch-and-bound guided by the Extended Gilmore–Lawler Bound"
  - url: /assets/images/research/logistics/qap_bounds.jpg
    image_path: /assets/images/research/logistics/qap_bounds.jpg
    alt: "Subgradient and lower-bound evolution"
    title: "Lagrangian lower/upper bounds under different step sizes"
gallery_qfd:
  - url: /assets/images/research/logistics/qfd_framework.jpg
    image_path: /assets/images/research/logistics/qfd_framework.jpg
    alt: "Two-phase robust fuzzy QFD framework"
    title: "Two-phase robust fuzzy QFD based on the mean-end-chain concept"
  - url: /assets/images/research/logistics/qfd_fuzzy.jpg
    image_path: /assets/images/research/logistics/qfd_fuzzy.jpg
    alt: "Fuzzy random importance ratings"
    title: "Fuzzy random importance ratings and their distributions"
---

> **Goal:** design supply chains and logistics services that are *on time, synchronized and solvable at real-world scale*, by pairing rigorous formulations (VI, QAP, MINLP) with decomposition algorithms that exploit network structure.

<div class="notice--primary" markdown="1">
**At a glance:** (1) synchronized service network design and large-scale decomposition algorithms · (2) perishable supply chains and multi-echelon distribution location · (3) service design with robust fuzzy QFD.
</div>

## 1. Supply Chain

### 1.1 Synchronized service network design & decomposition algorithms

In a transshipment hub, **inbound and outbound services must be scheduled together** so that goods are sorted and forwarded without long waits. I developed a **network-based QAP (NET-QAP)** that linearizes the classic Koopmans–Beckmann QAP and generalizes it, then solves it with an **Extended Gilmore–Lawler Bound (EGLB)** inside branch-and-bound.

{% include gallery id="gallery_qap" layout="half" caption="**Wu**, Lu, Wu & Zhou (2021), *Transportation Research Part B*." %}

**Insight:** viewing synchronization as an *assignment of services to timeslots* turns a hard scheduling problem into a QAP with a network structure, and that structure yields tight bounds and an efficient exact search.

Where should each food product be produced, which DC should serve which train, and how much should be replenished at each stop, when **pedestrian congestion** in stations slows handling? A nonlinear MIP on a lot-sizing network is decomposed by **Lagrangian substitution**.

{% include gallery id="gallery_lot" layout="third" caption="**Wu**, Nie, Xu & Zhao (2019), *Transportation Research Part E*." %}

{% include figure image_path="/assets/images/research/logistics/qap_physical.jpg" alt="Physical network with pick-up stations, DCs and warehouses" caption="Large-scale synchronized network: 20 pick-up stations, 12 distribution centers and 16 warehouses (**Wu** et al., 2021, *TR-B*)." popup=true %}

- **Wu, X.**, Lu, J., Wu, S., Zhou, X.S. (2021). Synchronizing time-dependent transportation services: Reformulation and solution algorithm using quadratic assignment problem. *Transportation Research Part B*, 152, 140–179. [DOI](https://doi.org/10.1016/j.trb.2021.08.008)
- **Wu, X.**, Nie, L., Xu, M., Zhao, L. (2019). Distribution planning problem for a high-speed rail catering service considering time-varying demands and pedestrian congestion: A lot-sizing-based model and decomposition algorithm. *Transportation Research Part E*, 123, 61–89. [DOI](https://doi.org/10.1016/j.tre.2019.01.003)
- Jiang, Y., He, T., Xiong, J., **Wu, X.**, Chen, Y. (2020). Parallel machine production and transportation operations' scheduling with tight time windows. *Complexity*, 2020, 1381340. [DOI](https://doi.org/10.1155/2020/1381340)

### 1.2 Perishable supply chains & multi-echelon distribution location

Every day, meals must move from suppliers to distribution centers (DCs), to rail stations, and onto **thousands of trains with tight time windows and deadlines**. A three-echelon location-routing model builds the distribution network directly from the train timetable.

{% include gallery id="gallery_catering" layout="half" caption="**Wu**, Nie & Xu (2017), *Transportation Research Part C*." %}

{% include figure image_path="/assets/images/research/logistics/catering_network_map.jpg" alt="Distribution network on the Beijing–Shanghai corridor" caption="Candidate DCs and rail stations along the Beijing–Shanghai high-speed line." popup=true %}

A **variational inequality (VI)** model captures the equilibrium of a perishable food supply chain with **uncertain on-train demand** (newsvendor) and **path time-deadline constraints** under flow-dependent lead times. Deadlines are reformulated with the Dirac delta function so they can be dualized, and the model is solved by an **Euler algorithm with an augmented Lagrangian dual**. The case study covers 246 trains on the Beijing–Shanghai corridor.

{% include gallery id="gallery_pfsc" layout="half" caption="**Wu**, Nie, Xu & Yan (2018), *Transportation Research Part E*." %}

**Insight:** freshness is a *path* constraint, not an arc constraint. Writing it in VI form shows how deadlines reshape equilibrium flows and profits.

- **Wu, X.**, Nie, L., Xu, M., Yan, F. (2018). A perishable food supply chain problem considering demand uncertainty and time deadline constraints: Modeling and application to a high-speed railway catering service. *Transportation Research Part E*, 111, 186–209. [DOI](https://doi.org/10.1016/j.tre.2018.01.002)
- **Wu, X.**, Nie, L., Xu, M. (2017). Designing an integrated distribution system for catering services for high-speed railways: A three-echelon location routing model with tight time windows and time deadlines. *Transportation Research Part C*, 74, 212–244. [DOI](https://doi.org/10.1016/j.trc.2016.11.006)
- Jiang, Y., **Wu, X.**, Chen, Y. (2020). Designing a flexible catering system for high-speed railway considering departure time selection and time deadline constraints. *IEEE Access*, 8, 44300–44317. [DOI](https://doi.org/10.1109/ACCESS.2020.2978180)

### 1.3 Service design & quality function deployment (QFD)

For **service design**, such as choosing service stations and DC locations, customer requirements are translated into technical decisions under **fuzziness and randomness**, using a two-phase robust fuzzy QFD based on the mean-end-chain concept.

{% include gallery id="gallery_qfd" layout="half" caption="**Wu**, Nie & Xu (2017), *European Journal of Operational Research*." %}

- **Wu, X.**, Nie, L., Xu, M. (2017). Robust fuzzy quality function deployment based on the mean-end-chain concept: Service station evaluation problem for rail catering services. *European Journal of Operational Research*, 263(3), 974–995. [DOI](https://doi.org/10.1016/j.ejor.2017.05.036)
- **Wu, X.**, Nie, L., Xu, M. (2015). Service station evaluation problem in catering service of the high-speed railway: a fuzzy QFD approach based on evidence theory. *Mathematical Problems in Engineering*, 2015, 404926. [DOI](https://doi.org/10.1155/2015/404926)
- **Wu, X.**, Nie, L., Xu, M., Fu, H. (2016). Fuzzy QFD for distribution center location evaluation in catering service of high-speed railway. *Management & Engineering*, 22, 83.

---
*Figures are reproduced from the author's own publications for scholarly, non-commercial illustration; please cite the original articles.*
