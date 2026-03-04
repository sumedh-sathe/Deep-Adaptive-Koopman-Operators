# Deep-Adaptive-Koopman-Operators
A deep meta-learning framework that learns updates over Koopman operators, enabling fast adaptation of nonlinear dynamics models under dynamic regime shifts

## Background: Koopman Operator Theory
 - Koopman operator theory represents nonlinear dynamics linearly in a lifted latent space.
 - States and controls are mapped into a higher-dimensional latent representation where the Koopman operator acts linearly.
 - This makes complex dynamics more interpretable and a natural fit for prediction, planning, and control.
 - Classical Koopman models are typically trained offline and do not model uncertainty or online adaptation.

## Formulation
|##Formulation I | Formulation II|
|:---:|:---:|
