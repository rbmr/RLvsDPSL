# RL vs DPSL

This an unfinished paper written as a follow-up to my [bachelor's thesis paper](https://repository.tudelft.nl/record/uuid:82e0d46c-a1f4-46c9-aaa6-fbdcd8a81012).

While working on the Bachelor's thesis I discovered it was possible to efficiently approximate the optimal trading strategy in intraday trading scenarios given perfect lookahead using dynamic programming (DP). The idea for future work I posed in the thesis was to train a supervised model instead of a reinforcement learning model, using this dynamic programming approximation as the ground truth. This became Dynamic Programming-based Supervised learning (DPSL). One could view this as having access to the optimal value function, and using it to determine the optimal policy. The idea then became to compare the performance of this DPSL technique with the standard reinforcement learning (RL) techniques I attempted in my thesis. The main issue with the thesis however was that the models were only using past prices in their prediction of future prices. In many markets, getting postive PnL using this method is generally impossible. The issue was the lack of predictive power in the features, and DPSL did not solve is. As a consequence, both the DPSL and RL methods performed poorly, and since the bottleneck lied elsewhere, the comparison was largely irrelevant. Leading to me to drop the project.

Since I still really like the idea of being able to find the perfect trading strategy, under the assumptions of zero market impact, and perfect lookahead, and using this to train trading models, I am publishing this unfinished work here.

The code I wrote for implementing and testing the DPSL approach is available here: https://github.com/rbmr/SupervisedFX
