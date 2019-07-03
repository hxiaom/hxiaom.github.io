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

2. [Zheng Y, Capra L, Wolfson O, et al. Urban computing: concepts, methodologies, and applications[J]. ACM Transactions on Intelligent Systems and Technology (TIST), 2014, 5(3): 38.](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/UrbanComputing-zheng-tist2014.pdf)

    - Motivation:
        - Introduce urban computing
    - Concepts:
        - Urban computing is an interdisciplinary field where computer sciences meet conventional city-related fields, like transportation, civil engineering, environment, economy, ecology, and sociology in the context of urban spaces
    - Methodologies:
        - urban sensing
        - urban data management
        - knowledge fusion across heterogeneous data
        - urban data visulization
    - Applications:
        - urban planning
        - transportation
        - the environment
        - energy
        - social
        - economy
        - public safety and security
        - presenting representative scenarios in each category

3. [Wang X, Liu W, Yang H, et al. Customer behavioural modelling of order cancellation in coupled ride-sourcing and taxi markets[J]. Transportation Research Part B: Methodological, 2019.](https://www.sciencedirect.com/science/article/pii/S0191261518311330)

    - Motivation: understand customer order cancellation behavior
    - Methods:
        - Data analysis
        - Modeling
    - Results:
        - The mean ride distance and pick-up distance of cancelled orders are observed to be obviously longer than those of completed orders of the same time period, reflecting an obvious impact of travel cost on customer decisions of order cancellation. 
        - The correlation between the mean customer confirmed-order cancellation rate (COCR) and the mean customer waiting time for pick-up of cancelled orders is significantly negative. an outcome of the lower (higher) chance of meeting vacant taxis while waiting for pick-up during peak (non-peak) hours.