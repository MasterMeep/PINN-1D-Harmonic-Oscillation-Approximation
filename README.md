# PINN-1D-Harmonic-Oscillation-Prediction
Using a PINN the network learns to predict the position of a 1d harmonic oscillator using 10 ground truth data points (sampled from the ground truth) and 100 collocation points for the pde loss function. this method of function prediction generated u(t) given a small amount of samples from the real solution f(t) (i.e from the solved equation of real world measurements) where u(t) ~ f(t). in this project the model is trained both knowing and predicting the fiction coefficient of the system

# Base Example: 0.0004 loss -- 20,000 epochs -- lr 1e-3
![image](https://github.com/MasterMeep/PINN-1D-Harmonic-Oscillation-Prediction/assets/51376656/ed68ddd2-aaa2-4453-b1c0-d9bf40b64aa2)

# Learning coefficient of friction

one of the biggest strengths of a PINN is being able to treat the parameters of the system as learnable parameters of the model. In this case forcing the model to learn μ (the friction coefficient of the system) along side solving the ODE. Even while doing this however it produced accurate results in the same amount of time as the base case.

learned μ: 4.09
actual μ: 4.00

![image](https://github.com/MasterMeep/PINN-1D-Harmonic-Oscillation-Approximation/assets/51376656/c2ed4217-69e4-4f39-9e53-26e034d90619)

# Learning coefficient of friction and spring constant: 40,000 epochs -- lr 1e-2

though much harder for PINN's the solve for, in this example the model trained μ and k and managed to get relatively accurate results after double the epochs, and 10x the learning rate. if given a little more epochs and a better optimized learning rate it would have been able to solve for this system just as well. 

learned μ: 4.12
actual μ: 4.00

learned k: 375.42
actual k: 400.0

![image](https://github.com/MasterMeep/PINN-1D-Harmonic-Oscillation-Approximation/assets/51376656/0538d35a-a3db-43c3-be1f-1531ee62b3ed)
