# multi-armed-bandit-epsilon-greedy

Multi-Armed Bandit Problem with Epsilon-Greedy Strategy
Overview
The multi-armed bandit (MAB) problem is a classic problem in reinforcement learning and decision-making. It represents a scenario where an agent must choose between multiple options (referred to as "arms"), each with an unknown probability of providing a reward. The objective is to maximize the cumulative reward over time by balancing exploration (trying out different arms) and exploitation (choosing the best-known arm).

Problem Definition
In this implementation, we have three bandits (arms) with different probabilities of yielding a reward:

Arm 1: Probability of success = 0.2
Arm 2: Probability of success = 0.5
Arm 3: Probability of success = 0.75
The challenge is to determine which arm to pull in each trial to maximize the total reward earned over a series of trials.

Epsilon-Greedy Strategy
The epsilon-greedy strategy is a popular approach to tackle the exploration-exploitation dilemma. Here’s how it works:

Exploration vs. Exploitation:

With probability 
𝜖
ϵ (epsilon), the agent explores by randomly selecting one of the arms to pull.
With probability 
1
−
𝜖
1−ϵ, the agent exploits by selecting the arm with the highest estimated probability of success based on past experiences.
Parameter 
𝜖
ϵ:

In this implementation, 
𝜖
ϵ is set to 0.1, meaning there is a 10% chance of exploring and a 90% chance of exploiting the best-known arm.
Estimation of Probabilities:

Each arm maintains an estimated probability of success, which is updated every time the arm is pulled based on the outcome (reward) received.
Implementation Details
In the provided code:

Bandit Class: Represents each arm with methods to pull the arm and update its estimated probability.
Run Simulation Function: Simulates the process of pulling arms over a defined number of trials (2000 in this case).
Counts how many times each arm is explored or exploited.
Tracks the total rewards and calculates win rates over time.
Plotting: At the end of the simulation, it plots the win rates and compares them to the optimal win rate, which is based on the highest true probability of success among the arms.
Results and Insights
After running the simulation:

You can observe the estimated probabilities of each bandit arm.
The total reward, overall win rate, and the counts of exploration and exploitation are printed out.
The plotted graph shows how the win rate evolves over time, allowing you to visualize the effectiveness of the epsilon-greedy strategy in identifying the best-performing arm.
Conclusion
This implementation of the multi-armed bandit problem using the epsilon-greedy strategy demonstrates a fundamental concept in reinforcement learning. It effectively balances exploration and exploitation, helping the agent learn and adapt its strategy based on the observed rewards.
