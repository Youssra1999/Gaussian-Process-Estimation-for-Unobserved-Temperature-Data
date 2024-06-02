# Gaussian Process Estimation for Unobserved Temperature Data

## Overview
This project explores the application of Gaussian processes to estimate unobserved temperature data in Boston. We utilize Gaussian processes to model temperature variations, leveraging historical averages and observations from 2019.



<img src="_Genomics and High Dimensional Data (2).png" alt="Image" width="100" align="right">


## Data
We work with temperature data from two sources:
1. Weather information in Boston from 1981 to 2010, providing average high and low temperatures.
2. Weather information in Boston in 2019, offering daily average high and low temperatures.

The provided dataset ('data.mat') contains 365 rows and 4 columns, representing consecutive days of the year.

## Model
- We model temperature for each day as a Gaussian random variable.
- Historical average data serves as a surrogate mean for the random variables.
- 2019 temperature data serves as observations.

## Kernel Function for Covariance Matrix
- We select a kernel function to model the covariance matrix, crucial for Gaussian process modeling.
- The chosen function depends on parameters a and ell, impacting the shape of the kernel function.

## Cross Validation
- We partition the available observations for cross-validation, facilitating model evaluation.
- Observations are split into two groups for simplicity.

## Conditional Distribution
- We compute the conditional mean and variance of Partition 1 given Partition 2.
- Parameters theta1, theta2, and theta3 influence the conditional distributions.

## Parameter Optimization
- We evaluate parameter performance using the log marginal likelihood as a merit function.
- A brute force approach is employed to test a range of parameter values.

## Estimating Unobserved Data
- With optimized parameters, we generate estimates for unobserved temperatures.
- Components of the covariance matrix are separated with optimal parameters.
- Conditional means and variances are computed, yielding estimates for unobserved temperatures.

## Performance Evaluation
- Finally, we evaluate the performance of the model against observed data.

