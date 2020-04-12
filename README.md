[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/43851646-d899bf20-9b00-11e8-858c-29b5c2c94ccc.png "Crawler"


# Continuous Control

### Introduction

This project implements a deep reinforcement learning policy gradient algorithm Deep Deterministic Policy Gradient (DDPG) which can operate over continuous action spaces.

### The environment

The algorithm is trained with [Reacher](https://github.com/Unity-Technologies/ml-agents/tree/0.4.0/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The environment contains 20 identical agents, each with its own copy of the environment. The experiences of all agent is used to train a single model

### Solving the Environment

The environment is considered solved, when the average (over 100 episodes) of average score of the 20 agents is at least +30. 

## Getting Started

1. Download the environment.

```bash
wget https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip
```

Note that with this agent you will not be able to watch the agent.

2. Install requirements

```bash
pip install -r requirements.txt
```

3. Start the notebook

```bash
jupyter notebook
```

Open the notebook Reacher-training.ipynb.

## Licenses and acknowledgements

- The code is based on [Udacity Deep Reinforcement Learning nanodegree](https://github.com/udacity/deep-reinforcement-learning/) materials and is thus continued to be licensed under [MIT LICENSE](LICENSE).

## Author

- [tjkemp](https://github.com/tjkemp)
