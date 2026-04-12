# rydberg-parameter-lab

Parameter-space exploration of driven Rydberg atom systems with open-system dynamics and quantum information applications.

---

## Overview

This repository studies light–atom interactions in neutral-atom platforms using Rydberg excitation. The focus is on how system behavior evolves across key physical parameters:

- Rabi frequency (Ω)
- Detuning (Δ)
- Rydberg interaction strength (V)
- Dissipation and decoherence rates (γ)

By mapping parameter landscapes, this project connects physical modeling → open-system dynamics → performance metrics relevant to quantum information tasks.

---

## Physical Model

### Driven Two-Level System

The basic Hamiltonian in the rotating frame:

H = (Ω/2) σ_x - Δ |r⟩⟨r|

where:
- Ω: Rabi frequency (drive strength)
- Δ: detuning
- |r⟩: Rydberg state

---

### Two-Atom Rydberg Interaction

For two atoms:

H = Σ_i [(Ω/2) σ_x^(i) - Δ n_i] + V n_1 n_2

where:
- V: Rydberg–Rydberg interaction (blockade strength)
- n_i = |r⟩⟨r|_i

---

### Open-System Dynamics (Lindblad)

Time evolution:

dρ/dt = -i[H, ρ] + Σ_k (L_k ρ L_k† - 1/2 {L_k† L_k, ρ})

Typical channels:
- spontaneous emission
- dephasing

---

## Core Capabilities

- Single-atom Rabi dynamics
- Multi-level Rydberg excitation
- Two-atom blockade modeling
- Open quantum system simulation (Lindblad)
- Parameter sweeps and phase diagrams
- Gate fidelity evaluation
- Parameter optimization

---

## Key Workflows

### 1. Parameter Scans
Explore system response over (Ω, Δ, V, γ)

### 2. Blockade Regime Identification
Quantify suppression of double excitation

### 3. Open-System Effects
Analyze decoherence and performance degradation

### 4. Gate Fidelity Landscapes
Compute fidelity of target states or operations across parameter space

### 5. Optimization
Identify high-performance regions and refine parameters

---

## Repository Structure

```
rydberg-parameter-lab/
├── README.md
├── docs/
├── notebooks/
│   ├── 01_single_atom_scan.ipynb
│   ├── 02_blockade_regime.ipynb
│   ├── 03_open_system_dynamics.ipynb
│   ├── 04_fidelity_landscape.ipynb
│   └── 05_parameter_optimization.ipynb
├── src/rydberg_parameter_lab/
│   ├── hamiltonians.py
│   ├── lindblad.py
│   ├── parameters.py
│   ├── scans.py
│   ├── blockade.py
│   ├── metrics.py
│   ├── optimize.py
│   └── plotting.py
├── figures/
├── tests/
└── environment.yml
```

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

## Roadmap

- [ ] Implement single-atom solver
- [ ] Two-atom blockade simulation
- [ ] Lindblad open-system module
- [ ] Fidelity benchmarking tools
- [ ] Parameter landscape visualization
- [ ] Pulse optimization layer
- [ ] Reproducible benchmark suite

---

## Research Direction

This project is structured to support:

- physically grounded modeling of neutral-atom systems  
- analysis of tradeoffs between coherence, interaction strength, and control  
- reproducible evaluation of quantum information performance  

The emphasis is on clarity of physical assumptions, numerical stability, and interpretable results.

---

## License

MIT License
