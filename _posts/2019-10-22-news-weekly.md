---
layout: post
title: 2019.10 News Weekly 5
categories: Mobility
---

1. [Bengio、Sutton的深度学习&强化学习暑期班又来了，2019视频已放出](https://www.jiqizhixin.com/articles/2019-10-27-3)

2. Krarup, Benjamin, et al. "Towards Model-Based Contrastive Explanations for Explainable Planning."
    
    - Motivation: Producing contrastive explanation like "Why action A instead of action B?" requires the generation of the constrastive plan.
    - Research question: complile user question to constraints in a temporal and numeric PDDL2.1 planning setting
    - Methods:
        - To give contrastive explanation is to reason about what would happen in the counterfactual cases.
        - The authors approach this problem by generating plans for counterfactual cases via compilations, which they call the hypothetical model, or HModel.

3. [读博一时爽，不听这些建议会一直爽……](https://www.jiqizhixin.com/articles/2019-10-28-10)

4. [联合利华、高盛等 100 多家公司都在用 AI 面试官，靠谱吗？](https://www.jiqizhixin.com/)

5. [哈工大张伟男：人机对话关键技术及挑战](https://www.jiqizhixin.com/articles/2019-10-30-8)

5. [当博弈论遇上机器学习：一文读懂相关理论](https://www.jiqizhixin.com/articles/2019-10-28-9)

6. [黄奇帆：中国央行很可能在全球第一个推出数字货币](https://ishare.ifeng.com/c/s/v002IfL91DiW8h5JhPhinUuMb248Vs-_xLXcaV9FzhbxlLTA__)

7. Nair, Suraj, et al. "Causal Induction from Visual Observations for Goal Directed Tasks." arXiv preprint arXiv:1910.01751 (2019).

    - Motivation: causal reasoning is an indispensable capability for intelligence.
    - Research quesiton: causal reasoning for completing goal-directed tasks.
    - Methods
        - 1) an iterative causal induction model with attention, which learns to incrementally update the predicted causal graph for each observed interaction in the environment,
        - 2) a goal-conditioned policy with an attention-based graph encoding, forcing it to focus on the relevant components of the causal graph at each step.
        
8. [MIT 6.S093: Introduction to Human-Centered Artificial Intelligence (AI)](https://www.youtube.com/watch?v=bmjamLZ3v8A)

9. [给中央领导讲课陈纯的演讲全文：链上、链下数据协同技术是联盟链发展重要方向](https://mp.weixin.qq.com/s/U5rg1T2uBOEpJCDMklqTww)

10. Cai, Carrie J., et al. "Human-centered tools for coping with imperfect algorithms during medical decision-making." Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems. ACM, 2019.

    - Motivation: algrithmically decision is different with doctor's decision on retrieve visually similar medical images from past patients.
    - Methods: 
        - identified the needs of pathologists when searching for similar images retrieved using a deep learning algorithm
        - developed tools that empower users to cope with the search algorithm on-the-fly, communicating what types of similarity are most important at different moments in time.
            - refine-by-region
            - refine-by-example
            - refine-by-concept
    - contribution:
        - enumerate key needs of pathologists when searching for similar images during medical decision-making.
        - present the design and implementation of interactive refinement tools, including a novel technique, refine-by-concept, that leverages key affordances of deep neural network models for similarity search.
        - report results from two studies demonstrating that these refinement tools can increase the utility of clinical information found and increase user trust in the algorithm, without a loss in diagnostic accuracy. Overall, experts perferred SMILY over a traditional interface, and indicated they would be more likely to use it in clinical practice.
        - identify ways that experts used refinement tools for purposes beyond refining their searches, including testing and understanding the underlying search algorithm; investigating the likelihood a decision hypothesis; and disambiguating ML errors from their own errors.

11. [Waymo expands self-driving services to include B2B car parts delivery trial](https://techcrunch.com/2019/10/29/waymo-expands-self-driving-services-to-include-b2b-car-parts-delivery-trial/)

12. [数字货币，通俗易懂](https://www.weibo.com/tv/v/IdZBXgbTK?fid=1034:4433350782325389)

13. Madumal, Prashan, et al. "A Grounded Interaction Protocol for Explainable Artificial Intelligence." Proceedings of the 18th International Conference on Autonomous Agents and MultiAgent Systems. International Foundation for Autonomous Agents and Multiagent Systems, 2019.

    - Motivation: XAI needs interation.
    - Research question: the challenges of meaningful interaction between an explainer and an explainee
        - key components that makeup an explanation interaction protocol (locutions)
        - relationships within those components (termination rules)
        - component sequences and cycles (combination rules)
    - Method:
        - grounded thoery
        - formalize the model using the agent dialogue framework (ADF) as a new dialogue type and then evaluate it in a human-agent interaction study.
        - propose a interaction protocol for the socio-cognitive process of explanation that is derived from different types of natural conversations between humans as well as humans and agents.

14. [机器学习模型可解释性的详尽介绍](https://www.jiqizhixin.com/articles/2019-10-30-9)

15. Neverova, Natalia, et al. "Learning human identity from motion patterns." IEEE Access 4 (2016): 1810-1820.

    - Motivation: learning human identity from motion patterns
    - challenges:
        - efficiently learning task-relevant representations of noisy inertial data;
        - incorporating them into a biometrics setting, characterized by limited resources. Limitations include how computational power for model adaptation on a new user and for real-time inference, as well as the absence (or very limited amount) of "negative" samples.
    - Method:
        - introduce the first method for active biometric authentication with mobile inertial sensors.
