# Gaussian State Preparation

## Introduction
State Preparation is a cornerstone of quantum algorithms and applications, enabling the initialization of quantum systems into specific states as a starting point for subsequent operations. Its efficiency directly impacts the accuracy and scalability of quantum computations.

A particular interest is the Gaussian state preparation, which is essential for simulating physical systems and tackling problems in quantum chemistry, machine learning, and optimization. Gaussian states, characterized by their Gaussian-shaped wavefunctions, are powerful tools for encoding probability distributions and modeling quantum systems.

This project leverages Classiq's quantum computing SDK to implement a Gaussian state preparation in the interval [-2, 2).

## Target State: The Gaussian State Representation
The Gaussian state is defined as:

\[
|x_0\rangle_N = |0\rangle_N \longrightarrow \sum_{|x\rangle_N} \sqrt{G(x)} |x\rangle_N
\]

Where \( G(x) \) is represented as a vector:

\[
{G}(x_i) = \frac{\exp(-\lambda \cdot {x_i}^2)}{\sum_{x' \in \text{domain}} \exp(-\lambda \cdot (x')^2)} \text{, for } x_i \in \text{domain}
\]

- \( G(x) \) is the normalized Gaussian vector across the discrete domain.  
- \( \vec{x} \) represents the set of discrete points in the domain.  
- \( \lambda \) represents the decay rate, controlled by the variable `EXP_RATE`, which determines the spread of the Gaussian.
- The denominator ensures normalization across the entire domain.

## Installation
To use this project, ensure you have the required dependencies installed:

```sh
pip install classiq


## Authentication

If running for the first time, authenticate with Classiq:

import classiq
# classiq.authenticate()  # Uncomment to authenticate

## Running the Code

Run the Jupyter Notebook to execute the Gaussian state preparation algorithm. The implementation initializes and prepares the quantum system in a Gaussian state within the specified interval.

License

This project is intended for educational and research purposes. Please ensure compliance with any relevant licensing agreements for the Classiq SDK.

