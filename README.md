# Unified-Gas-Storage-Valuation-Framework

**Latest Update (April 2026):** *Revised repository for peer review. Includes new misclassification robustness checks and corrected extreme-tail visualization logic.*

A unified real options valuation framework for natural gas storage integrating Hidden Markov Models (HMM), cross-market spillover indices, and Stochastic Dynamic Programming (SDP). Official implementation code for the paper.

**Supplementary Material for Manuscript:** *"A Unified Real Options Framework for Natural Gas Storage: Integrating Market Regimes and Cross-Market Spillovers"*

## Overview
This repository contains the Python implementation of the **Regime-Switching Stochastic Dynamic Programming (SDP)** framework presented in the paper. The code allows for the replication of:
1. **Synthetic Data Generation** (Log-Mean Reversion with Jump Diffusion).
2. **HMM Calibration** (Regime Identification).
3. **Valuation** (Backward Induction & Monte Carlo Simulation).

## Repository Structure
- **`Paper1_Unified_Framework-Updated.ipynb`**: The master Jupyter Notebook containing the full implementation.
  - **Module A:** Data Generation (Eq. 2)
  - **Module B:** Regime Identification (HMM)
  - **Module C:** SDP Valuation Algorithm (Algorithm 2)
  - **Module D:** Forward Simulation (Table 4 Results)
  - **Module E:** Robustness Checks (New)

## Quick Start
1. **Valuation (Table 4):**
   - Uses `numpy.random.seed(42)` to reproduce the +197% NPV result.
   - **Run:** Cell 10

2. **Misclassification Robustness Check (Table 4 Ablation):**
   - Simulates the degraded 30.0% accuracy scenario to prove structural resilience.
   - **Run:** Cell 11

3. **Visualization (Figure 2):**
   - Uses `numpy.random.seed(100)` to generate the representative "Structural Break" path shown in the manuscript.
   - **Run:** Cell 5

## Requirements
- Python 3.8+
- numpy
- pandas
- scipy
- matplotlib
- seaborn
- scikit-learn *(Required for KMeans initialization)*
