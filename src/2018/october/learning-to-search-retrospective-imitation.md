# Learning to Search via Retrospective Imitation

Brief background given on RL and IL.

## Imitation Learning

Initially, learn a policy based off of supervised learning.  Use a "human
expert" to demonstrate some examples of desired actions.

This is problematic because the testing data will eventually diverge from the
training set.  DAgger (Data Aggregation) will correct the original policy by
playing some reinforcement learning sessions and then ask the human to label
some of them.

How can we do this with less expert data? 

## Retrospective Imitation

Idea: policy practices and reflects on its mistakes

# Multi-fidelity Bayesian Optimization with Gaussian Processes
Motivation: Interested in doing inferences on proteins.  Issues:  
* costly to synthesize and measure actual proteins
* simulations also costly
