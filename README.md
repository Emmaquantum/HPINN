# Learning Specialized Activation Functions for Physics informed Neural Networks

## Overview
Physics-Informed Neural Networks (PINNs) train machine learning models to solve complex physical systems, such as fluid dynamics, heat transfer, and wave propagation. However, getting these models to train reliably usually requires engineers to manually guess and test internal settings known as activation functions.

This project implements an alternative **Adaptive Blending Units (ABU-PINN)**, a flexible architecture that enables neural networks to automatically build and fine-tune their own custom activation functions during training.

---

## Key Value & Features
- **Eliminates Manual Tuning**: Replaces manual trial-and-error by dynamically blending multiple candidate activation functions into a single optimal shape.
- **Stabilizes Training**: Resolves severe gradient imbalance issues that typically cause standard physics-informed networks to fail or stall.
- **Tailored Precision**: Automatically adapts its internal dynamics to fit the exact physics equation being modeled.

---

## Performance Results
Evaluated across standard mathematical physics benchmarks, this self-tuning architecture consistently outperformed traditional fixed-activation models:

| Physics Simulation Problem | Error Reduction vs. Best Standard Model |
| :--- | :--- |
| **Convection Equation** | **83% error reduction** |
| **Cahn-Hilliard Equation** | **56% error reduction** |
| **KdV (Wave) Equation** | **46% error reduction** |

*Note: The adaptive blending step increases computation time by approximately 3x compared to standard setups. This trade-off makes it ideal for high-precision engineering applications where simulation accuracy is paramount.*

---

## Detailed Report
For a slide deck detailing the network architecture, eigenvalue stability analysis, and complete experimental benchmarks, refer to the project summary document:
- 📄 [Main Presentation PDF (main (1).pdf)](./main%20(1).pdf)
