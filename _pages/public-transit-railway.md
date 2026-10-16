---
layout: single
title: "Public Transit & Railway Management"
permalink: /public-transit-railway/
author_profile: true
toc: true
toc_sticky: true
toc_label: "Research Threads"
excerpt: "Equity-driven transit pricing, railway demand learning, seat allocation, line planning, timetabling, air–rail integration, and urban air mobility."
header:
  overlay_image: /assets/images/research/banner_transit.jpg
  overlay_filter: 0.45
  caption: "Estimated boarding, alighting and OD demand on the Beijing–Shanghai high-speed rail corridor (Wu et al., 2025, TR-E)"
gallery_tec:
  - url: /assets/images/research/transit/tec_concept.jpg
    image_path: /assets/images/research/transit/tec_concept.jpg
    alt: "Tradable Equity Credit scheme"
    title: "The TEC market: agencies earn credits by beating equity targets and buy credits when they fall short"
  - url: /assets/images/research/transit/tec_credit.jpg
    image_path: /assets/images/research/transit/tec_credit.jpg
    alt: "Equity credit and equity debt under baseline-and-credit"
    title: "Baseline-and-credit: equity credit (+) vs. equity debt (–)"
gallery_tec_case:
  - url: /assets/images/research/transit/tec_network.jpg
    image_path: /assets/images/research/transit/tec_network.jpg
    alt: "Transit network case study"
    title: "Case-study transit network: service links, transfers, and census-tract centroids"
  - url: /assets/images/research/transit/tec_pies.jpg
    image_path: /assets/images/research/transit/tec_pies.jpg
    alt: "Population group composition by census tract"
    title: "Heterogeneous traveler groups by census tract"
gallery_rail:
  - url: /assets/images/research/transit/rail_induced.jpg
    image_path: /assets/images/research/transit/rail_induced.jpg
    alt: "Induced, diverted and ex-post demand"
    title: "Decomposing ridership: baseline, diverted, induced and ex-post demand"
  - url: /assets/images/research/transit/rail_cg_layers.jpg
    image_path: /assets/images/research/transit/rail_cg_layers.jpg
    alt: "Five-layer constrained computational graph"
    title: "Constrained CG: boarding → OD → train-line → alighting → line-segment layers"
gallery_seat:
  - url: /assets/images/research/transit/seat_inventory.jpg
    image_path: /assets/images/research/transit/seat_inventory.jpg
    alt: "Seat inventory as SKUs on train segments"
    title: "Seats as SKUs: one seat can serve several OD products along a train"
  - url: /assets/images/research/transit/seat_network.jpg
    image_path: /assets/images/research/transit/seat_network.jpg
    alt: "Resources, products and itineraries including transfers"
    title: "Resources → products → itineraries, including transfer itineraries"
gallery_line:
  - url: /assets/images/research/transit/line_bjsh.jpg
    image_path: /assets/images/research/transit/line_bjsh.jpg
    alt: "Beijing–Shanghai HSR network"
    title: "Beijing–Shanghai HSR and connecting directions"
  - url: /assets/images/research/transit/line_stops.jpg
    image_path: /assets/images/research/transit/line_stops.jpg
    alt: "Optimized stop patterns"
    title: "Optimized train stop patterns for a large-scale line plan"
gallery_airrail:
  - url: /assets/images/research/transit/airrail_timetable.jpg
    image_path: /assets/images/research/transit/airrail_timetable.jpg
    alt: "Passenger routing across train, shuttle bus and flight"
    title: "Door-to-gate routing: train → shuttle bus → flight, with adjusted timetables"
  - url: /assets/images/research/transit/airrail_network.jpg
    image_path: /assets/images/research/transit/airrail_network.jpg
    alt: "HSR network with Zhengding Airport station"
    title: "Real-world case: HSR network serving Zhengding Airport"
  - url: /assets/images/research/transit/airrail_bg_timetable.jpg
    image_path: /assets/images/research/transit/airrail_bg_timetable.jpg
    alt: "Optimized train diagrams on two corridors"
    title: "Optimized train diagrams: Beijing–Guangzhou and Tianjin–Taiyuan corridors"
  - url: /assets/images/research/transit/airrail_jat.jpg
    image_path: /assets/images/research/transit/airrail_jat.jpg
    alt: "Adjusted rail timetable for air–rail synchronization"
    title: "Timetable adjustment to synchronize trains with flights"
gallery_uam:
  - url: /assets/images/research/transit/uam_concept.jpg
    image_path: /assets/images/research/transit/uam_concept.jpg
    alt: "Multimodal service integrating HSR and UAM"
    title: "Vertiports feed HSR stations: a multimodal UAM + HSR service"
  - url: /assets/images/research/transit/uam_beijing.jpg
    image_path: /assets/images/research/transit/uam_beijing.jpg
    alt: "Vertiports and railway stations in Beijing–Tianjin–Hebei"
    title: "Candidate vertiports and HSR stations in the Beijing–Tianjin–Hebei region"
  - url: /assets/images/research/transit/uam_solution.jpg
    image_path: /assets/images/research/transit/uam_solution.jpg
    alt: "Optimized vertiport–station connections"
    title: "Optimized vertiport–station hub assignments without/with capacity constraints"
gallery_cn:
  - url: /assets/images/research/transit/cn_china_map.jpg
    image_path: /assets/images/research/transit/cn_china_map.jpg
    alt: "Chinese railway network as a complex network"
    title: "China's railway system as a weighted complex network"
  - url: /assets/images/research/transit/cn_core_periphery.jpg
    image_path: /assets/images/research/transit/cn_core_periphery.jpg
    alt: "Core–periphery structure"
    title: "Core–periphery structure of the railway network"
---

> **Goal:** make public transit and railways *fair, efficient and seamless*, from how agencies are funded, to how seats, lines and timetables are planned, to how rail connects with airports and future air taxis.

<div class="notice--primary" markdown="1">
**At a glance:** Tradable Equity Credits (TECs) · railway demand learning on constrained computational graphs · seat inventory control · line planning · timetabling and air–rail integration · urban air mobility (UAM) + high-speed rail (HSR) · complex-network analysis.
</div>

## 1. Tradable Equity Credits (TECs) for Public Transit

A **market-based equity policy**: agencies earn credits by surpassing equity targets and incur debts when they fall short; credits are priced and traded. Nonlinear programming models let agencies maximize farebox revenue *and* meet equity goals, with **dynamic pricing for heterogeneous travelers**.

{% include gallery id="gallery_tec" layout="half" caption="The TEC baseline-and-credit mechanism (**Wu** et al., 2026, *TR-E*; **Wu** et al., 2025, *Transportmetrica A*)." %}

{% include gallery id="gallery_tec_case" layout="half" caption="Case study: equity-aware subsidy and pricing across census tracts with different population groups." %}

**Insight:** unlike fixed subsidies, TECs reward *measurable* equity improvement and let agencies trade. The TEC price converges to an equilibrium, and inequality indices fall without sacrificing revenue.

- **Wu, X.**, Liu, K., Zhen, D., Ji, Y.E., Cui, Q., Xiong, C. (2026). Tradable Equity Credits (TECs) for public transit: a dynamic pricing approach for heterogeneous travelers. *Transportation Research Part E*, 211, 104858. [DOI](https://doi.org/10.1016/j.tre.2026.104858)
- **Wu, X.**, Liu, K., Zhen, D., Ji, Y., Shang, X., Cui, Q., Xiong, C. (2025). Tradable Equity Credits (TECs) and internalised revenue maximisation: a nonlinear programming model for promoting equitable public transit services. *Transportmetrica A: Transport Science*. [DOI](https://doi.org/10.1080/23249935.2025.2537413)
- Zhen, D., **Wu, X.**, Liu, K., Ji, Y., Xiong, C., Cui, Q. (2026). Carbon credit in travel demand management: an incentive-based framework for emission reduction. *Transportation Research Part D*, 150, 105041. [DOI](https://doi.org/10.1016/j.trd.2025.105041)
- Hu, S., Xiong, C., Ji, Y., **Wu, X.**, Liu, K., Schonfeld, P. (2024). Understanding factors influencing user engagement in incentive-based travel demand management program. *Transportation Research Part A*, 186, 104145. [DOI](https://doi.org/10.1016/j.tra.2024.104145)

## 2. Railway Demand Learning on Computational Graphs

Ridership changes for three reasons: **diverted** demand (travelers switch lines), **induced** demand (better service creates new trips), and **ex-post** demand (seat limits force second choices). A constrained computational graph estimates all three at once, together with boarding/alighting, OD trips and train-line loads.

{% include gallery id="gallery_rail" layout="half" caption="**Wu**, Wang, Kim, Saleh, Fu & Xiong (2025), *Transportation Research Part E*." %}

{% include figure image_path="/assets/images/research/transit/rail_demand_map.jpg" alt="Estimated boarding, alighting and OD demand on Beijing–Shanghai HSR" caption="Learned boarding, alighting and OD demand on the Beijing–Shanghai high-speed rail corridor." popup=true %}

**Insight:** separating induced from diverted demand tells planners whether a new line *grows* the market or only *reshuffles* it, which is critical for line-plan and fare decisions.

## 3. Seat Inventory Control & Ticket Allocation

Railway seats are network resources shared by many OD products. Dynamic **bid-price** control decides, in real time, whether to sell a ticket, including **transfer itineraries** across trains.

{% include gallery id="gallery_seat" layout="half" caption="Yuan, Nie, **Wu** & Fu (2018), *PLOS ONE*." %}

- Yuan, W., Nie, L., **Wu, X.**, Fu, H. (2018). A dynamic bid price approach for the seat inventory control problem in railway networks with consideration of passenger transfer. *PLOS ONE*, 13(8), e0201718. [DOI](https://doi.org/10.1371/journal.pone.0201718)
- Yuan, W., Nie, L., **Wu, X.** (2018). A dynamic bid price approach for the seat inventory control problem in high-speed railway networks considering passenger transfer service. *TRB 97th Annual Meeting*. [TRID](https://trid.trb.org/View/1494499)
- Yuan, W., Nie, L., Fu, H., **Wu, X.**, Ke, Y. (2018). Simulation-based method for seat inventory control optimization under heterogeneous customer behavior: a case study of the China Railway. *CICTP 2018*, 788–798.

## 4. Line Planning

Which trains run, and where do they stop? Line-planning models balance **direct service for diverse OD demand** against operating cost on large HSR networks, from daily to **weekly** plans.

{% include gallery id="gallery_line" layout="half" caption="Zhang, Nie, **Wu** & Ke (2020), *Networks and Spatial Economics*: flexible stopping patterns on the Beijing–Shanghai HSR." %}

- Zhang, X., Nie, L., **Wu, X.**, Ke, Y. (2020). How to optimize train stops under diverse passenger demand: a new line planning method for large-scale high-speed rail networks. *Networks and Spatial Economics*, 20(4), 963–988. [DOI](https://doi.org/10.1007/s11067-020-09506-5)
- Nie, B., Nie, L., Fu, H., **Wu, X.** (2023). Weekly line planning to improve the match between rail supply and passenger demand. *Computer-Aided Civil and Infrastructure Engineering*, 38(13), 1810–1833. [DOI](https://doi.org/10.1111/mice.12941)

## 5. Timetabling & Air–Rail Integration

Passengers connect from high-speed trains to flights through shuttle buses and walking. Integrated **time–space network** models synchronize *train, aircraft, shuttle and passenger* flows, solved by **ADMM** decomposition.

{% include gallery id="gallery_airrail" layout="half" caption="Ke, **Wu**, Nie, Yao & Chen (2024), *TR-C*; Ke, Nie, Liebchen, Yuan & **Wu** (2020), *Journal of Advanced Transportation*." %}

**Insight:** small, coordinated timetable shifts on rail produce many more valid air–rail connections; adding shuttle-bus capacity sharply reduces the number of unrouted passengers.

- Ke, Y., **Wu, X.**, Nie, L., Yao, Z., Chen, Y. (2024). Synchronizing train, aircraft, shuttle, and passenger flows in intermodal timetabling: A time–space network-based formulation and a decomposition algorithm using ADMM. *Transportation Research Part C*, 159, 104464. [DOI](https://doi.org/10.1016/j.trc.2023.104464)
- Ke, Y., Nie, L., Liebchen, C., Yuan, W., **Wu, X.** (2020). Improving synchronization in an air and high-speed rail integration service via adjusting a rail timetable: A real-world case study in China. *Journal of Advanced Transportation*, 2020, 5081315. [DOI](https://doi.org/10.1155/2020/5081315)

## 6. Urban Air Mobility (UAM) + High-Speed Rail (New, 2026)

Electric VTOL air taxis can feed HSR stations. A **hub-and-spoke network design** model assigns vertiports to stations via a **semi-quadratic assignment** formulation, made tractable by exploiting the special UAM–HSR network structure in its linearization.

{% include gallery id="gallery_uam" layout="third" caption="**Wu**, Huo, Wen & Xing (2026), *Urban Rail Transit*: case studies in the Beijing–Tianjin–Hebei and Yangtze River Delta regions." %}

- **Wu, X.**, Huo, Y., Wen, Y., Xing, J. (2026). Multimodal hub-and-spoke network design problems to integrate urban air mobility and high-speed rail services: A semi-quadratic assignment formulation and its linearization. *Urban Rail Transit*. [DOI](https://doi.org/10.1007/s40864-026-00270-2)

## 7. Railway Networks as Complex Systems

{% include gallery id="gallery_cn" layout="half" caption="Wang, Cai, Du, **Wu** et al. (2020), *Chaos, Solitons & Fractals*: scale-free and core–periphery structure of the Chinese railway system." %}

- Wang, W., Cai, K., Du, W., **Wu, X.**, Tong, L.C., Zhu, X., Cao, X. (2020). Analysis of the Chinese railway system as a complex network. *Chaos, Solitons & Fractals*, 130, 109408. [DOI](https://doi.org/10.1016/j.chaos.2019.109408)

---
*Figures are reproduced from the author's own publications for scholarly, non-commercial illustration; please cite the original articles.*
