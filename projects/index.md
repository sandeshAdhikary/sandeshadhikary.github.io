---
layout: default
title: Projects
description: Projects
---
Here's a summary of some of my projects

### Policy Composition in Multi-Objective Reinforcement Learning
As we expand the scale and complexity of problems tackled by reinforcement learning, the 
[reward hypothesis](http://incompleteideas.net/rlai.cs.ualberta.ca/RLAI/rewardhypothesis.html) 
will continue to be put to the test: can we always find a single reward signal to encapsulate any 
objective? We are routinely faced with multiple competing objectives, but only fuzzy notions of the ultimate composite goal. 
Economic policy must bolster growth while curbing inequality; robots must reach goals while avoiding obstacles around them; 
financial investment strategies must maximize returns but with a diverse portfolio. Even if a single reward
function does exist for such problems, it may be quite difficult to define. 

A promising solution is to train separate agents for different objectives, and find a way to combine their policies into a composite policy. 
Much of the current literature on policy-composition focuses on defining weighted averages of value functions for individual objectives. 
We are interested in expanding this strategy to encode notions such as stability, fairness, co-operation, and so on. 
Our aim is to define a structured class of policy composition strategies which we can use to design novel policy composition strategies
in a principled manner, going beyond simple (Euclidean) value-averaging. 

### Geometry-Aware Sampling with Kernel Herding
Riemannian manifolds crop up routinely in various domains, robotics being a prime example. 
Various properties of a robot such as its orientation (spherical manifold), full pose (SE(3) manifold), 
its damping and inertia matrices (symmetric positive definite manifold), can be modeled as elements of 
Riemannian manifolds. We exploit such geometric structure for the task of drawing samples from empirical 
distributions via the kernel herding algorithm. Kernel herding uses Frank-Wolfe optimization to generate samples from an empirical distribution (i.e. weighted data points), using a kernel function to define similarity between samples. We adapted this process for sampling over Riemannian manifolds by (1) using kernels that use the appropriate notion of distance on the manifold, and (2) using Riemannian optimization techniques to ensure samples always lie on the manifold. This geometry-aware adaptation of kernel herding can be used in various problems that require sampling from empirical distributions (e.g. particle filtering, approximate Bayesian inference of simulator parameters, etc.).

#### Links:
[Workshop paper in RSS 2021](https://sites.google.com/view/geotopo-rss2021/accepted-contributions) | 
Full paper under review

### Quantum Tensor Networks for Probabilistic Modeling

Quantum tensor networks (QTNs) are factorizations of very large tensors, generally the joint wave-functions
 of multiple entangled quantum particles. 
The simplest of these tensor networks, called matrix product states (MPS), decomposes tensors into a series of matrix products. 
Variants of MPS have also been adapted for classical probabilistic modeling in learning compressed representations of joint probability tensors over sequences. 
The natural question thus arises: how do these differ from existing machine models such as stochastic processes and weighted automata? 
By identifying the inherent tensor network structure of these probabilistic models, we develop formal connections and 
relative expressiveness relationships between models across the different fields.

#### Links:
[Conference paper in AISTATS 2021](https://proceedings.mlr.press/v130/adhikary21a) | 
[Workshop paper in Neurips 2022](https://tensorworkshop.github.io/NeurIPS2021/accepted_papers/TP_LPDOs__QTNML_2021_(4).pdf)

### Learning Hidden Quantum Markov Models on the Stiefel Manifold
In our exploration of quantum-inspired probabilistic models, we found hidden quantum Markov models (HQMMs)
 to be a particularly useful model class. Among the alternatives we’ve considered, these are the most 
 expressive class of linear models that are not plagued by the negative probability problem, i.e., they 
 produce non-negative probabilities by design. However, when learning HQMMs from data, we need to ensure these models result in distributions that are 
also _normalized_. This constraint can be imposed by utilizing additional geometric structure
 of HQMMs -- we can identify their parameters as elements of the Stiefel manifold. We 
 demonstrated how gradient descent over Riemannian manifolds (which includes the Stiefel manifold) can be
  used to feasibly learn HQMMs. This approach is not only more accurate than the prior approach, but also requires substantially
   less time to train.
   
#### Links:
[Conference paper in AISTATS 2020](https://proceedings.mlr.press/v108/adhikary20a.html)

