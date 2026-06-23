Benchmarking Avalanche Characteristics of Memristive Devices: Validation of Criticality

Author: Prashanth Prasannakumar

Institution: Department of Computational and Data Sciences, Indian Institute of Science (IISc), Bangalore

Year: 2026

Overview

This repository contains the official codebase and the complete dissertation PDF for the thesis titled "Benchmarking Avalanche Characteristics of Memristive Devices: Validation of Criticality."

This project provides a standardized, multi-layered data analysis pipeline to address challenges in neuromorphic engineering, specifically regarding the identification, quantification, and optimization of the "edge of chaos" operating regime in memristive hardware. The pipeline achieves the following:

Ingests raw electrical measurements and isolates discrete memristive switching avalanches.

Validates Self-Organized Criticality (SOC) through rigorous Maximum Likelihood Estimation (MLE) of power-law distributions.

Reconstructs multi-dimensional phase spaces to demonstrate deterministic chaos (Lyapunov exponents, Surrogate testing).

Demonstrates that physical Reservoir Computing (RC) performance peaks at the critical boundary.

Repository Structure

The provided Python scripts replicate the physical constraints and empirical findings of the thesis. They are categorized into four modules:

Module 1: Signal Processing & Avalanche Extraction

avalanche_extraction.py: Implements adaptive localized variance thresholding to filter thermal noise and isolate discrete switching events (size $S$ and duration $T$).

Module 2: Statistical Mechanics & Universality (SOC)

mle_power_law_fitting.py: Implements discrete MLE to extract power-law exponents without regression bias.

universality_scaling.py: Benchmarks empirical distributions, demonstrating Mean Field Theory (MFT) for Ag-hBN and Directed Percolation (DP) for Nanowire Networks.

crackling_noise_scaling.py: Validates the scaling relationship $\gamma = (\alpha - 1)/(\tau - 1)$.

avalanche_shape_collapse.py: Demonstrates universality via temporal rescaling of avalanches onto a single function.

Module 3: Phase-Space Reconstruction & Chaos Theory

ami_time_delay.py: Computes Average Mutual Information (AMI) for optimal phase space embedding.

fnn_embedding_dimension.py: Determines the optimal embedding dimension ($m$) using False Nearest Neighbors.

rosenstein_lyapunov.py: Tracks trajectory divergence to extract the Largest Lyapunov Exponent ($\lambda_{max}$).

surrogate_testing.py: Rejects the null hypothesis of linear stochastic noise using IAAFT surrogate data.

Module 4: In-Materia Reservoir Computing

ipc_tradeoff.py: Visualizes the bias-variance tradeoff between "fading memory" and "non-linear separability".

spatial_criticality_heatmap.py: Maps spatially tunable criticality across a multi-electrode mesh.

u_shaped_error_curve.py: Benchmarks predictive performance (NARMA-10), demonstrating error minimization at the critical voltage boundary.

Installation & Usage

Prerequisites

The code requires standard scientific Python libraries:

pip install numpy matplotlib scipy seaborn


Execution

Execute the scripts to generate the publication-ready data visualizations:

python u_shaped_error_curve.py
Department of Computational and Data Sciences

Indian Institute of Science (IISc), Bangalore
