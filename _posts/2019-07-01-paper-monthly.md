---
layout: post
title: 2019.07 Paper
categories: Mobility
---

1. [CoRide: Joint Order Dispatching and Fleet Management for Multi-Scale Ride-Hailing Platforms](https://arxiv.org/pdf/1905.11353.pdf)

    - Motivation: 
        - optimally dispatch orders to vehicles 
        - trade off between immediate and future returns
    - Method:
        - model ride-hailing as a large-scale parallel ranking problem
        -  study the joint decisionmaking task of order dispatching and fleet management
    - unique challenges:
        - First, to facilitate a huge number of vehicles to act and learn efficiently and robustly, we treat each region cell as an agent and build a multi-agent reinforcement learning framework.
        - Second, to coordinate the agents from different regions to achieve long-term benefits, we leverage the geographical hierarchy of the region grids to perform hierarchical reinforcement learning. 
        - Third, to deal with the heterogeneous and variant action space for joint order dispatching and fleet management, we design the action as the ranking weight vector to rank and select the specific order or the fleet management destination in a unified formulation. 
        - Fourth, to achieve the multi-scale ride-hailing platform, we conduct the decision-making process in a hierarchical way where a multi-head attention mechanism is utilized to incorporate the impacts of neighbor agents and capture the key agent in each scale