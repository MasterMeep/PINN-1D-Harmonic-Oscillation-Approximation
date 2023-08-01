# PINN-1D-Harmonic-Oscillation-Prediction
Using a PINN the network learns to predict the position of a 1d harmonic oscillator using 10 ground truth data points (sampled from the ground truth) and 100 collocation points for the pde loss function. this method of function prediction is an analytic solution where the model learns a function u(t) which approximates the solved differential f(t) withouth having access to more than the original differential along with a small set of real data points to ground the final output.

# Example -- 0.0004 loss -- 99.99% accuracy -- 20,000 epochs -- lr 1e-3
![image](https://github.com/MasterMeep/PINN-1D-Harmonic-Oscillation-Prediction/assets/51376656/ed68ddd2-aaa2-4453-b1c0-d9bf40b64aa2)
