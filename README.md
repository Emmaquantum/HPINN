# High-Performance Neural Networks for Complex Wave Dynamics (MABUR-PINN V2)

## Overview
Simulating complex physical phenomena—such as acoustic waves, fluid turbulence, and quantum fields—usually requires immense computational power. Physics-Informed Neural Networks (PINNs) offer a faster alternative by embedding physical laws directly into deep learning models. 

However, standard PINNs frequently struggle with wave propagation, leading to unstable training and inaccurate predictions.

This project introduces **MABUR-PINN V2** (*Modified Adaptive Blending Units Residual PINN*), an advanced deep learning architecture designed to solve complex wave dynamics reliably. By combining self-tuning activation functions with adaptive skip connections, the model dynamically learns wave frequencies and stabilizes the training process.

---

## Key Performance Improvements

Tested against standard wave physics benchmarks (Klein-Gordon equation), **MABUR-PINN V2** achieved top-tier precision, dramatically outperforming both standard baseline models and modern state-of-the-art architectures:

| Architecture | Relative Error ($L_2$) | Absolute Error | Final Loss | Status |
| :--- | :--- | :--- | :--- | :--- |
| **MABUR-PINN V2 (Our Model)** | **1.70%** | **0.0006** | **3.81e-07** | **Best Performance** |
| ABU-PINN | 2.14% | 0.0008 | 4.60e-07 | Baseline |
| Modified MLP (M4) | 4.41% | 0.0013 | 2.21e-06 | Baseline |
| SIREN PINN | 21.20% | 0.0068 | 5.85e-06 | Baseline |
| Multi-Scale Fourier PINN | 43.20% | 0.0142 | 9.99e-05 | Baseline |
| Standard (Vanilla) PINN | 71.00% | 0.0232 | 6.72e-05 | Failed |

### Main Highlights
- **41x Precision Increase**: Reduced model relative error from **71.00%** (Standard PINN) down to **1.70%**.
- **Outperformed Modern Benchmarks**: Superior accuracy compared to specialized architectures like ABU-PINN (2.14%) and M4-PINN (4.41%).
- **Lowest Final Loss**: Reached the lowest convergence loss ($3.81 \times 10^{-7}$) with high parameter efficiency (149k parameters vs 2.1M in Multi-Scale setups).

---

## Technical Innovation & Architecture
1. **Self-Tuning Activations**: Dynamically blends sine, cosine, hyperbolic tangent, and rational functions so the network automatically adapts to both smooth trends and rapid oscillations.
2. **Adaptive Residual Connections**: Gradually introduces non-linear complexity during training, preventing gradient vanishing and initialization failures.
3. **Smart Spatial Sampling**: Prioritizes computational resources within active wave propagation zones (light-cones) for faster and more accurate learning.

---

## Real-World Value & Applications
- **Engineering & Acoustics**: High-fidelity wave simulation with significantly lower computational overhead.
- **Fluid & Energy Systems**: Improved modeling of turbulent or high-frequency physical dynamics.
- **Data-Driven Physics**: Scalable architecture adaptable to complex forward and inverse engineering problems.

---

## Project Resources
- **GitHub Repository**: [HPINN Project on GitHub](https://github.com/Emmaquantum/HPINN)
- **Detailed Research Paper**: For complete theoretical derivations, loss curves, and experimental setups, view the full report [main (2).pdf](./main%20(2).pdf).
