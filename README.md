# rydberg-parameter-lab

Parameter-space exploration of driven Rydberg atom systems with open-system dynamics and quantum information applications.

---

## Overview

This repository studies light–atom interactions in neutral-atom platforms using Rydberg excitation, with a focus on **noise-robust phase-locked CZ gates**.

We explore how system behavior organizes across key physical parameters:

- Rabi frequency (Ω)
- Detuning (Δ)
- Rydberg interaction strength (V)
- Dissipation and decoherence rates (γ, γφ)
- Control duration (T) and pulse shape parameters

The project connects:
**physical modeling → open-system dynamics → reduced scaling laws → quantum gate performance**

---

## 🔹 New Result: Emergent Low-Dimensional Structure

Across Notebooks 22–33, we find that noisy gate performance is governed by an approximate **low-dimensional scaling law**.

### 1. Effective Noise Coordinate

Noise collapses onto a single direction:

    γ_eff = γ + λ · γφ

This reduces a 2D noise space → 1D.

---

### 2. Control Rescaling

Across control variations (T, α, Ω):

    x = γ_eff · (T / T_c)

where:
- T_c = extracted phase-lock survival boundary

---

### 3. Emergent Scaling Law

For most protocols:

    S ≈ Ŝ(γ_eff · T / T_c)

where:
- S = phase-lock order parameter (fidelity × coherence × (1 − leakage))
- Ŝ = shared response curve

---

### 4. Controlled Breakdown

Scaling is not exact.

A structured deviation appears for:
- short-duration protocols (low T)

This indicates a **missing physical dimension** (e.g. non-adiabatic effects).

---

## 🔹 Interpretation

This is not a trivial collapse.

Instead:

> System dynamics organize onto a **low-dimensional manifold**, with a **boundary where reduction fails**.

---

## Physical Model

### Driven Two-Level System

H = (Ω/2) σ_x − Δ |r⟩⟨r|

### Two-Atom Interaction

H = Σ_i [(Ω/2) σ_x^(i) − Δ n_i] + V n₁ n₂

### Open-System (Lindblad)

dρ/dt = −i[H,ρ] + Σ_k (L_k ρ L_k† − ½{L_k†L_k,ρ})

---

## Core Capabilities

- Rydberg dynamics simulation
- Open-system Lindblad evolution
- CZ gate modeling and compensation
- Noise robustness analysis
- Parameter sweeps and phase diagrams
- Scaling-law discovery
- Universality testing

---

## Key Workflows

### 1. Parameter Scans
Explore system response over (Ω, Δ, V, γ, γφ)

### 2. Open-System Effects
Analyze decoherence and performance degradation

### 3. Gate Fidelity Landscapes
Evaluate CZ fidelity under noise

### 4. Effective Coordinate Discovery
Identify reduced descriptions (γ_eff)

### 5. Scaling Collapse
Test universality across control parameters

### 6. Boundary Extraction
Locate phase-lock survival thresholds

---

## Repository Structure

```
rydberg-parameter-lab/
├── notebooks/
│   ├── 18–21   noise robustness + order parameter
│   ├── 22–23   effective noise collapse
│   ├── 24–26   optimal collapse direction
│   ├── 27–29   universality breakdown
│   ├── 30–32   boundary scaling laws
│   └── 33      full scaling collapse
```

---

## Current Status

- Effective noise coordinate identified  
- Near-universal scaling law discovered  
- Phase boundary extracted  
- Structured breakdown isolated  

---

## Next Step

Extend scaling to include a third variable:

    S = Ŝ(γ_eff · T/T_c, additional_dimension)

Likely candidates:
- adiabaticity (1/T)
- pulse curvature
- control bandwidth

---

## Installation

```bash
pip install -r requirements.txt
```

or

```bash
conda env create -f environment.yml
conda activate rydberg-parameter-lab
```

---

## Dependencies

- Python 3.10+
- NumPy
- SciPy
- Matplotlib
- QuTiP

---

## License

MIT License
