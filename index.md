# Valuing American Option by LSM Algorithm

### Introduction

Valuing the derivatives with American option features has been a main concern in financial industry for a long time. The major issue is to determine when is the optimal time to exercise the option. To accomplish this task, at any time point within option's time to maturity, people need to compare the option immediate exercise value to the discounted conditional continued expectation value from last time point.

The paper, ["Valuing American Options by Simulation: A Simple Least-Squares Approach"](https://people.math.ethz.ch/~hjfurrer/teaching/LongstaffSchwartzAmericanOptionsLeastSquareMonteCarlo.pdf), has proposed a brand-new approach to estimate the option's conditional expectation using least squares regression method. We could then, compute the American option value by working in backwardation until reaching the initial exercise date.

### Python code to reproduce the Least Square Monte Carlo (LSM) approach

Inspired by the Longstaff-Schwartz(2001) Least Square Monte Carlo (LSM) approach, this python notebook builds a simple and generalized pricing framework for the American (put) option by working in backwardation. 

Simulate the underlying stock price paths by Geometric Brownian motion.

To test the accuracy of this reproduced LSM algorithm, I try to run the numerical example of American put option used in paper. This algorithm did give the same initial value approximately $0.1144 as the results stated in the paper.
