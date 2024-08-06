# Accelerate 2024

This is part of [Accelerate 2024](https://www.accelerate24.ca/), in partnership with 
the [Acceleration Consortium](https://acceleration.utoronto.ca/) and 
[Merck KGaA, Darmstadt, Germany](https://www.emdgroup.com/en).

Code is based on the open-source experimental planner [BayBE](https://github.com/emdgroup/baybe).

# Workshop: Advanced Bayesian Optimization Recipes for Real-World Applications with BayBE

The workshop contains 1 quick start and 4 notebooks containing code examples
dealing with the following problems.

## 1 - Quick Start
Illustrating BayBE's basic components, the `searchspace`, `objective` and the
`recommender`, as well as our utility to generate simulation results for backtesting
different settings.

## 2 - Categorical Encodings
Categorical encodings are an easy way to introduce domain knowledge, such as chemical
intuition into the model. BayBE comes with builtin cheminformatics descriptors for
small molecules, particularly useful for all use cases where the choice of substance is
a parameter. The idea of encoding can be generalized to any domain of expertise,
not just chemistry, and a custom encoding is also demonstrated.

## 3 - Slot-Based Mixtures
Mixtures are an extremely common use case for Bayesian optimization. This notebook
introduces the difference between the traditional, purely number-based mixture
representation and slots. We illustrate the challenges arising from the slot-based
representation and how to address them with constraints. When created correctly, the
slot-based representation can make use of smart encodings and also model the order of
addition naturally. 

## 4 - Dynamic Campaign Stopping
Realizing when a campaign should be stopped can be trivial if the absolute targets were
met. However, it is much less clear how to realize that continuing a campaign is
unpromising if no convergence to the optimum has happened. Here, we use a simple
criterion based on the pointwise probability of improvement to stop a campaign. We
will utilize BayBE's custom hook mechanic to inject the check.

## 5 - Transfer Learning
Transfer learning in the context of Bayesian optimization denotes situations where data
from similar-but-not-quite-the-identical campaigns is available when starting a new
optimization. This is a situation prevalent in industry, as data from similar
campaigns, such as similar reactions, cell-lines, locations etc., is in principle
available but usually untapped.