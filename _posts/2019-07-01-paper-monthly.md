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
        - Modelling
    - Results:
        - The mean ride distance and pick-up distance of cancelled orders are observed to be obviously longer than those of completed orders of the same time period, reflecting an obvious impact of travel cost on customer decisions of order cancellation. 
        - The correlation between the mean customer confirmed-order cancellation rate (COCR) and the mean customer waiting time for pick-up of cancelled orders is significantly negative. an outcome of the lower (higher) chance of meeting vacant taxis while waiting for pick-up during peak (non-peak) hours.

4. [Wang S, Meng Q, Yang H. Global optimization methods for the discrete network design problem[J]. Transportation Research Part B: Methodological, 2013, 50: 42-60.](https://www-sciencedirect-com.ezproxy.cityu.edu.hk/science/article/pii/S0191261513000179)

    - Motivation: multi-capacity discrete network design problem
    - Proposed Method: 
        - bi-level programming model
            - the upper level aims to minimize the total travel time via adding new lanes to candidate links
            - the lower level is a traditional Wardrop user equilibrium (UE) problem
        -  two global optimization methods by taking advantage of the relationship between UE and system optimal (SO)
            - SO-relaxation, exploits the property that an optimal network design solution under SO principle can be a good approximate solution under UE principle, and successively sorts the solutions in the order of increasing total travel time under SO principle
            - UE-reduction, adds the objective function of the Beckmann-McGuire-Winsten transformation of UE traffic assignment to the constraints of the SO-relaxation formulation of the multi-capacity DNDP.

5. [Ke J, Zheng H, Yang H, et al. Short-term forecasting of passenger demand under on-demand ride services: A spatio-temporal deep learning approach[J]. Transportation Research Part C: Emerging Technologies, 2017, 85: 591-608.](https://www.sciencedirect.com/science/article/pii/S0968090X17302899)

    - Motivation: Short-term passenger demand forecasting
    - Method: 
        - fusion convolutional long short-term memory network (FCL-Net). 
        - Fusion of convolutional LSTM layers, standard LSTM layers and convolutional layers. 
        - Better capture spatio-temporal correlations of explanatory variables.
        - A tailored spatially aggregated random forest is used to rank feature importance.
        - Applied to real-world on-demand ride service data provided by DiDi.

6. [A general model of demand-responsive transportation services: From taxi to ridesharing to dial-a-ride](https://www.sciencedirect.com/science/article/pii/S0191261518307793)

    - Motivation: a general analytic framework to model transit systems that provide door-to-door service.
    - Method: the framework yields approximate closed form formulas for many cases of interest.

7. [Modelling car-following behaviour of connected vehicles with a focus on driver compliance](https://www.sciencedirect.com/science/article/pii/S0191261518306362)

    - Motivation: connected vehicle driving, driver compliance
    - Method:
        - A novel connected vehicle driving strategy (CVDS) is developed.
        - Driver compliance is modelled using the prospect theory.

8. [Profit-oriented fixed-charge network design with elastic demand](https://www.sciencedirect.com/science/article/pii/S0191261518310130)

    - Motivation: elastic demand, fixed-charge multicommodity network
    - Method: Modelling