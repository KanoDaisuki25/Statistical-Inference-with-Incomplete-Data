# Statistical Inference with Incomplete Data

## Overview
This repo contains the analysis and R implementations for an assessment on **Incomplete Data Analysis**. The project focuses on statistical inference under various missing data mechanisms and censoring schemes, utilising both theoretical derivation and computational simulation in R.

## Key Topics & Implementations

### 1. Survival Analysis & Type I Censoring
- **Theory:** Derived the Probability Density Function (PDF) and Maximum Likelihood Estimators (MLE) for **Pareto-distributed** variables under Type I censoring (where $Z = \min(X, Y)$).
- **Inference:** Constructed asymptotic 95% confidence intervals for the shape parameters based on the Fisher Information matrix.

### 2. Multiple Imputation (MICE) Simulation Study
- **Goal:** Evaluated the empirical coverage probability of confidence intervals for regression coefficients ($\beta_1$).
- **Method:** Conducted a simulation study ($n=100$ datasets) comparing **Stochastic Regression Imputation** vs **Bootstrap-based Imputation** using the `mice` package.
- **Finding:** Analysed how acknowledging parameter uncertainty affects interval coverage under Missing At Random (MAR) mechanisms.

### 3. Left-Censored Data Analysis
- **Optimisation:** Implemented a custom Log-Likelihood function for **Left-Censored Normal Data** (where values below limit $D$ are reported as $D$).
- **Estimation:** Optimised the likelihood function using `optim`/`maxLik` to estimate the mean $\mu$ and variance $\sigma^2$ from the dataset `dataex3`.

### 4. Missing Data Mechanisms (Theory)
- Analysed Bivariate Normal samples to determine **Ignorability** for likelihood-based estimation under different missingness models (MAR vs MNAR) using logistic regression models for the missingness indicator $R$.

### 5. EM Algorithm for Logistic Regression
- **Algorithm:** Derived and implemented a custom **Expectation-Maximisation (EM) Algorithm** from scratch.
- **Application:** Estimated parameters for a Logistic Regression model where the binary response variable $Y$ has missing values (Bernoulli distribution).

## Tech Stack
- **R Libraries**: `mice` (Multiple Imputation), `maxLik` (Optimisation), `ggplot2`.

## Repo Structure
- `/code`: `.Rmd` files containing the analysis and code.
* `/data`: Datasets (`.Rdata`) used for the simulation and EM algorithm tasks.
* `/docs`: Final report and problem statements.

