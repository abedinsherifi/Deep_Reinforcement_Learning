# Deep Reinforcement Learning (DRL)

DRL uses Deep Neural Networks to come up with best actions for the agent. <br>

The Markov Decision Process (MDP) is a mathematical formulation of the RL problem. The Markov Property states that the current state is fully representative of the state of the environment. Hence, the future is only dependent on the present. <br>

S - State Space <br>
A - Action Space <br> 
R - Rewards for each pair of (S,A) <br>
P - Transition Probability <br>
Gamma - reward discount factor <br>

Gamma is between 0 and 1. A value of 1 for gamma means that immediate rewards are valued highest. A value of closer to 0 means that future rewards are valued highest. <br>

The objective of RL is to find an optimal policy that maximizes the cumulative discounted reward. A policy here is nothing else than a mapping of states to actions. <br>

Q-Learning is an off-policy algorithm for temporal difference (TD) learning which implies model free learning.

Q-Learning: <br>
    $$Q_{t+1}(s_t, a_t) = Q_{t}(s_t, a_t) + \alpha(r_{t+1} + \gamma max Q_{t}(s_{t+1},a) - Q_{t}(s_t, a_t)$$

Learning rate $\alpha$ specifies the learning rate for the agent of accepting new information over learnt information. <br>

Q-Learning Algorithm Steps:
- Initialize Q-Table with (s,a) all zeros per shape with size of states and actions
- Observe initial state s
- Perform action a
- Observe reward r and a new state $s_{t+1}$
- Update Q-Table with r and maximum reward from $s_{t+1}$

RL algorithms are based on exploration/exploitation concepts. <br>
Exploration is the finding of new information about the environment. <br>
Exploitation is the use of existing information to maximize the reward. <br>
