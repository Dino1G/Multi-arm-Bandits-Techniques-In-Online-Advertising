# Multi-arm Bandits Techniques In Online Advertising

## Abstract

This research paper explores the application of multi-armed bandit algorithms in optimizing content recommendations on online media platforms. The study aims to investigate the use of different bandit algorithms for dynamically selecting and adjusting content recommendations to maximize advertising revenue. A comprehensive experimental analysis is conducted, comparing the proposed methods against random approaches. The paper discusses the significance and potential benefits of utilizing multi-armed bandit algorithms in real-world recommendation systems. According to the experimental results, the ϵ-greedy algorithm demonstrates superior optimization capabilities compared to other Agent’s decision functions.

## Table of Contents

- [Introduction](#introduction)
- [Related Work](#related-work)
- [Methodology](#methodology)
  - [Data Collection](#data-collection)
  - [Agent’s Decision Function](#agents-decision-function)
  - [Modeling](#modeling)
- [Results/Analysis](#resultsanalysis)
- [Discussion](#discussion)
- [Conclusion](#conclusion)
- [Acknowledgments](#acknowledgments)
- [References](#references)

## Introduction

In response to the rapid growth of online media platforms, there has been a need for effective content recommendation systems that can personalize user experiences by suggesting relevant and engaging content. To address the exploration-exploitation trade-off in recommendation systems, multi-armed bandit algorithms have emerged as a promising approach [1].

## Related Work

Various multi-armed bandit (MAB) algorithms have been developed to tackle the exploration-exploitation trade-off and enhance content recommendations across different domains. Silva et al. (2022) offers a comprehensive explanation of the principles behind the MAB problem. The MAB problem is relevant in recommendation systems, where the objective is to maximize user satisfaction by dynamically selecting actions (e.g., recommending items) while learning and optimizing the recommendations [2].

## Methodology

### Data Collection

The Online Shoppers Purchasing Intention Dataset provided by UCL is utilized as the data source for this study. This dataset contains information from online shopping sessions, with a total of 12,330 instances. Among these sessions, 84.5% are negative class samples where shopping did not occur, while the remaining 15.5% are positive class samples ending with a purchase.

### Agent’s Decision Function

There are various agent’s decision functions in the MAB model. The methods employed in this study include the ϵ-greedy algorithm, Upper Confidence Bound (UCB), Uncertainty-Based Confidence-Bound Reinforcement Learning (UCBRL), and Thompson Sampling.

1. **ϵ-greedy algorithm**: The ϵ-greedy algorithm strikes a balance between exploration and exploitation by employing a probabilistic approach when selecting arms. It chooses the arm with the highest estimated reward with a probability of (1−ϵ) and opts for a random arm with a probability of ϵ.

2. **Upper Confidence Bound (UCB) algorithm**: The UCB algorithm relies on confidence intervals to estimate the upper bound of the expected reward associated with each arm. It selects the arm with the highest upper confidence bound.

3. **Uncertainty-Based Confidence-Bound Reinforcement Learning (UCBRL)**: UCBRL combines the principles of UCB algorithms with uncertainty estimation techniques. It estimates the upper confidence bound of the expected value of each action and selects actions based on these bounds.

4. **Thompson Sampling**: Thompson Sampling leverages Bayesian inference and assigns a probability distribution to each arm based on prior beliefs and observed rewards. The selection of an arm is determined by drawing samples from these probability distributions.

### Modeling

The conversion rates of different advertising arms are calculated by grouping the dataset by the 'Region' column and taking the mean of the 'Revenue' column. The results show that Ad9 has the highest conversion rate, which will be used to evaluate the effectiveness of the agent’s decision functions.

## Results/Analysis

The allocation of arms is observed using different agent’s decision functions. Figure 1 illustrates the selection frequencies of different arms by various agent’s decision functions. The ϵ-greedy algorithm yields the best results, allocating the highest number of selections to Ad9.

![Figure 1: The Number of Occurrences of Advertisements During The Trial](link-to-your-image.png)

The regret of different algorithms can be calculated by comparing the cumulative reward obtained by each algorithm with the cumulative reward that could have been achieved by always selecting the best arm. A lower regret indicates better performance of the algorithm in terms of maximizing rewards. According to Figure 2, the ϵ-greedy algorithm consistently exhibited lower regret compared to the other algorithms.

![Figure 2: Regret of Different Algorithms](link-to-your-image.png)

The total reward achieved by different algorithms refers to the cumulative sum of rewards obtained by each algorithm throughout the experimentation process. The results show that the ϵ-greedy algorithm achieved the highest total reward among the tested algorithms.

![Figure 3: Total Reward by Algorithms](link-to-your-image.png)

## Discussion

In the study, it was found that the ϵ-greedy algorithm performed the best among the different algorithms tested, followed by Thompson Sampling, Uncertainty-Based Confidence-Bound Reinforcement Learning (UCBRL), and Upper Confidence Bound (UCB) algorithm. Several possible reasons for this ranking were discussed, including the exploration and exploitation trade-off, optimistic bias, and robustness to uncertainty.

## Conclusion

According to the experimental results, the ϵ-greedy algorithm demonstrates superior optimization capabilities compared to other Agent’s decision functions, achieving a significantly higher reward value. The ϵ-greedy algorithm performs well because it strikes a balance between exploration and exploitation, allowing it to exploit the best-known actions while continuously exploring potentially better actions.

## Acknowledgments

I would like to express our gratitude to the University of California, Irvine (UCI) for providing the necessary resources and support for this project. The availability of the UCI dataset has been instrumental in conducting our research and analyzing the results.

## References

[1] R. C. Gatti, “A multi-armed bandit algorithm speeds up the evolution of cooperation,” Ecological Modelling, vol. 439, p. 109348, 2021.

[2] N. Silva, H. Werneck, T. Silva, A. C. Pereira, and L. Rocha, “Multi-armed bandits in recommendation systems: A survey of the state-of-the-art and future directions,” Expert Systems with Applications, vol. 197, p. 116669, 2022.

[3] D. I. Mattos, J. Bosch, and H. H. Olsson, “Multi-armed bandits in the wild: Pitfalls and strategies in online experiments,” Information and Software Technology, vol. 113, pp. 68–81, 2019.

[4] C. Yan, H. Han, Y. Zhang, D. Zhu, and Y. Wan, “Dynamic clustering based contextual combinatorial multi-armed bandit for online recommendation,” Knowledge-Based Systems, vol. 257, p. 109927, 2022.

[5] C. O. Sakar, S. O. Polat, M. Katircioglu, and Y. Kastro, “Real-time prediction of online shoppers’ purchasing intention using mult
