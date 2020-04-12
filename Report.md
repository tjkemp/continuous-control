# Report

## Learning algorithm

The implemented learning algorithm to solve the Reacher Unity environment is the Deep Deterministic Policy Gradient (DDPG) algorithm, first introduced by [research paper](https://arxiv.org/abs/1509.02971).

In the paper, they present an actor-critic, model-free algorithm based on the deterministic policy gradient that can operate over continuous action spaces.

The actor learns to approximate the best action for each state. The critic learns how to evaluate the action-value by using actions from the actor.

**Implementation details:**
- The actor model has two hidden layers, of size 128 and 64
- The critic model has three hidden layers, of size 64, 32 and 32
- Adam optimizer with learning rate 3e-4 is used for both models
- Batch size is 512
- Tau is 1e-3
- Replay buffer size is 1e5
- No weight decay

In contrast to the chosen parameters, the paper uses a larger layer sizes, and batch size of 64 for low dimensional problems.

## Plot of rewards

![Score plot](files/scores.png?raw=true "Plot of rewards")

The agent receives an average reward (over 100 episodes, and over all 20 agents) of +30 after 43 episodes of length 1000 steps. 

The environment can be considered solved.


## Ideas for future work

- Currently, at each time step, the parameters (of actor and critic) networks are updated. Better results may be achieved if the model is updated only half the time. That is, for ten steps, data is added into replay buffer, and then for ten steps update is performed. In 20 time steps, the network gets updated only ten times.
- The paper suggests using Batch Normalization in order to normalize each dimension across the samples in minibatch and perform well across different tasks.
- Systematic experimentation could lead to better hyperparameters. The suggestions by the paper should be excellent, but the suggested model is unnecessarily large, which slows the training for simple problems.
- Crawler environment would be an exciting (and more difficult) problem.
