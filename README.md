# RNP-Int

This repository contains the data and codes used in the paper.

## Simulation

`simulation data generation.nb` is used to generate simulation data. There are 200 covariates, four scenarios of y and three types of random errors. The survival data has an extra column indicates whether y is censored.

In `simulation data fitting.nb`, `SparseAdditiveModelFit` and `SparseAcceleratedFailureTimeModelFit` are two main functions. They have same inputs, but fit different models. The inputs and their meaning are as follows.
| Input | Meaning |
|---|---|
| data | Simulation data. |
| yType | 1, 2, 3, 4 correspond to different scenarios. |
| errorType | 1 for normal error, 2 for mixed error, 3 for Cauchy error. |
| methodType | 1 for NP-Int, 2 for NP-Meta, 3 for NP-Pool, 4 for P-Int. |
| lossType | 0 for robust loss function(R), 2 for non-robust loss function(NR). |
| q | Number of nodes.                                             |
| v | Step length. |
| T | Number of iterations. |
| lambda | Penalty parameter for unequal coefficients. |

`simulation data prediction.nb` and `simulation data table.nb` are used to evaluate the performance of the fit.

