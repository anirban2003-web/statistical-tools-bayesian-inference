# statistical-tools-bayesian-inference
# Statistical Tools & Bayesian Inference

This repository contains some of my practice work with **statistical methods and Bayesian parameter estimation**, with a focus on likelihoods, chi-square methods, and Markov Chain Monte Carlo (MCMC).

The notebooks are mainly computational exercises using cosmological data and simple cosmological models. They are intended as practice and methodological work rather than as a presentation of unpublished research results.

## Statistical Methods

The work in this repository covers several basic tools used in quantitative analysis:

- Chi-square minimization
- Likelihood functions
- Maximum-likelihood parameter estimation
- Bayesian priors and posterior probabilities
- Markov Chain Monte Carlo (MCMC)
- Parameter estimation for cosmological models
- Exploration of posterior distributions

The general Bayesian structure used in the MCMC exercises is

\[
P(\theta \mid D) \propto P(D \mid \theta)\,P(\theta),
\]

where \(P(D\mid\theta)\) is the likelihood and \(P(\theta)\) is the prior on the model parameters.

## Cosmological Parameter Estimation

Some of the exercises apply these methods to supernova distance-modulus data.

The analysis uses the cosmological expansion function \(E(z)=H(z)/H_0\), numerical integration to obtain the luminosity distance, and the distance modulus

\[
\mu = 5\log_{10}\left(\frac{D_L}{\mathrm{Mpc}}\right)+25.
\]

The likelihood is constructed from the difference between the observed and model distance moduli using the quoted observational uncertainties.

Two cosmological models are explored:

### ΛCDM

The first MCMC exercise estimates the matter density parameter \(\Omega_m\) for a flat ΛCDM model.

### XCDM

The second exercise extends the parameter space to estimate both

\[
\Omega_m
\]

and the dark-energy equation-of-state parameter

\[
w.
\]

The XCDM expansion history is implemented directly in the notebook and sampled using MCMC.

## Notebooks

### `Likelihood and Chi square(1).ipynb`

A basic exercise in likelihood and chi-square analysis.

The notebook demonstrates how to construct a chi-square function, vary a cosmological parameter, and identify the parameter value corresponding to the minimum chi-square.

### `LCDM_omega_m_estimation.ipynb`

MCMC parameter estimation for the matter density parameter \(\Omega_m\) in a flat ΛCDM model.

The notebook includes:

- Loading the supernova data
- Constructing the ΛCDM expansion function
- Numerical calculation of luminosity distance
- Calculation of distance modulus
- Construction of the likelihood
- Definition of a prior on \(\Omega_m\)
- MCMC sampling using `emcee`

### `XCDM_omega_m_and_w_estimation.ipynb`

Extension of the previous analysis to the XCDM model.

The notebook samples the two-dimensional parameter space

\[
(\Omega_m,w)
\]

using `emcee`, with the likelihood constructed from the difference between observed and model distance moduli.

### `HUBBLE DATA EMCEE(1).ipynb`

An initial MCMC notebook for working with Hubble-related data. This notebook is currently a minimal working file and may be expanded as the statistical exercises develop.

## Computational Tools

Python · NumPy · Pandas · SciPy · Matplotlib · Jupyter · emcee

## Repository Structure

```text
statistical-tools-bayesian-inference/
│
├── notebooks/
│   ├── Likelihood and Chi square(1).ipynb
│   ├── LCDM_omega_m_estimation.ipynb
│   ├── XCDM_omega_m_and_w_estimation.ipynb
│   └── HUBBLE DATA EMCEE(1).ipynb
│
├── figures/
│
├── data/
│
└── README.md
```

## Purpose

This repository is a collection of computational exercises used to develop practical experience with statistical inference, likelihood construction, Bayesian methods, and MCMC techniques in an astrophysical context.

The emphasis is on understanding how the statistical machinery is constructed and implemented in Python, rather than presenting these exercises as final scientific results.

---

**Anirban Mohonta Ayon**  
B.Sc. (Hons.) Physics, Ramjas College, University of Delhi
