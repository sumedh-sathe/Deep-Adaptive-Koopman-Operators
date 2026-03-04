# Deep-Adaptive-Koopman-Operators
A deep meta-learning framework that learns updates over Koopman operators, enabling fast adaptation of nonlinear dynamics models under dynamic regime shifts

## Background: Koopman Operator Theory
 - Koopman operator theory represents nonlinear dynamics linearly in a lifted latent space.
 - States and controls are mapped into a higher-dimensional latent representation where the Koopman operator acts linearly.
 - This makes complex dynamics more interpretable and a natural fit for prediction, planning, and control.
 - Classical Koopman models are typically trained offline and do not model uncertainty or online adaptation.

## Formulation
|**Formulation I**| **Formulation II**|
|:---:|:---:|
|![](https://github.com/sumedh-sathe/Deep-Adaptive-Koopman-Operators/blob/main/Images/formulation_I.png)|![](https://github.com/sumedh-sathe/Deep-Adaptive-Koopman-Operators/blob/main/Images/formulation_II.png)|
||Step 1 — Context Encoding: Encode past trajectories of states and actions into latent representations<br>Step 2 — Bayesian Meta-Update: Update the MNIW prior over the Koopman operator using recent data, yielding a posterior distribution over dynamics<br>Step 3 — Prediction & Planning: Roll out future latent states under the posterior Koopman operator and project them into the physical state space<br>Training Objective: Minimize the Negative Log-Likelihood (NLL) of trajectories under the predictive posterior, encouraging calibrated, adaptable Koopman dynamics|

