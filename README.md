# Gaussian State Preparation

## Introduction
State Preparation is a cornerstone of quantum algorithms and applications, enabling the initialization of quantum systems into specific states as a starting point for subsequent operations. Its efficiency directly impacts the accuracy and scalability of quantum computations.

A particular interest is the Gaussian state preparation, which is essential for simulating physical systems and tackling problems in quantum chemistry, machine learning, and optimization. Gaussian states, characterized by their Gaussian-shaped wavefunctions, are powerful tools for encoding probability distributions and modeling quantum systems.

This project leverages Classiq's quantum computing SDK to implement a Gaussian state preparation in the interval [-2, 2).

## Target State: The Gaussian State Representation
The Gaussian state is defined as:

|x₀⟩ₙ = |0⟩ₙ → ∑ |x⟩ₙ √G(x) |x⟩ₙ

Where G(x) is represented as a vector:

G(xᵢ) = exp(-λ ⋅ xᵢ²) / ∑ exp(-λ ⋅ x'²), for xᵢ in domain

- G(x) is the normalized Gaussian vector across the discrete domain.  
- x⃗ represents the set of discrete points in the domain.  
- λ represents the decay rate, controlled by the variable `EXP_RATE`, which determines the spread of the Gaussian.
- The denominator ensures normalization across the entire domain.

## Installation
To use this project, ensure you have the required dependencies installed:

```sh
pip install classiq

