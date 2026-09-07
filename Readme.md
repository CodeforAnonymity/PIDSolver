# PIDDPM-for-ACOPF

## Overview

This repository provides a simplified implementation of the method described in the paper:  
**"PIDSolver: A Sequential Physics-Informed Diffusion Solver for Optimization with Algebraic Constraints"**.

Due to GitHub's 25 MB file size limit, the dataset is **not** included in this repository. However, users can generate their own training and test data by running the `Data_Generator.jl` script.

---

## Repository Contents

| File | Description |
|------|-------------|
| `Data_Generator.jl` | Generates training and test datasets for the AC Optimal Power Flow (ACOPF) problem. |
| `Check_ACPF_Balance.py` | Verifies the correctness of the generated data by checking power‑flow balance constraints. |
| `PIDDPM-ACOPF_Solver-torch.py` | Main training and evaluation script. Running this file produces results for the IEEE 118‑bus system, similar to those reported in the paper. |

---

## Getting Started

1. **Generate data**  
   Run the Julia script to create your own datasets:
   ```bash
   julia Data_Generator.jl
   ```

2. **Verify data correctness** (optional)  
   Use the Python script to confirm that the generated power‑flow cases satisfy the balance equations:
   ```bash
   python Check_ACPF_Balance.py
   ```

3. **Train and evaluate the solver**  
   Execute the main PyTorch script to reproduce the IEEE 118‑bus results:
   ```bash
   python PIDDPM-ACOPF_Solver-torch.py
   ```

---

## Complete Code Release

The full codebase will be made publicly available upon acceptance of the paper.

---
