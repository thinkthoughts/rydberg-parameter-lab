# rydberg-parameter-lab

![Rydberg Parameter Lab](figures/banner.png)

Simulation and analysis of Rydberg atom interactions across control parameters (Ω, Δ, V, γ), including Lindblad dynamics and gate-fidelity landscapes for neutral-atom quantum computing.

---# rydberg-parameter-lab

![Rydberg Parameter Lab](figures/banner.png)

Simulation and analysis of Rydberg atom interactions across control parameters (Ω, Δ, V, γ), including Lindblad dynamics and gate-fidelity landscapes for neutral-atom quantum computing.

---

## Key Results

- Emergence of an **effective noise coordinate**: γ_eff = γ + λ·γ_φ  
- Identification of a **controlled breakdown** of 1D scaling at low T  
- Recovery via a **low-dimensional (2D) model** with near-perfect predictive accuracy  
- Extraction of a **curved phase boundary** not captured by linear effective-noise models  

---

## Overview

This project studies **noise-affected Rydberg CZ gates** and identifies **low-dimensional structure** in open-system quantum dynamics.

A central observation:

> System behavior approximately reduces from a 2D noise space  
> to a 1D effective coordinate, but this reduction fails in a  
> predictable regime and can be systematically repaired.

---

## Emergent Effective Noise Coordinate

![Effective noise collapse](figures/effective_noise_collapse.png)

Across a wide parameter range:

γ_eff = γ + λ·γ_φ

This defines a dominant direction in noise space governing system response.

---

## Breakdown of 1D Scaling

![1D failure](figures/1d_failure.png)

At low T:

- scaling curves fail to align  
- deviations are systematic  
- indicates missing structure beyond γ_eff  

---

## Low-Dimensional Model Recovery

![2D fit quality](figures/2d_fit_quality.png)

A simple 2D model restores accuracy:

- predicted vs true values align nearly perfectly  
- confirms system is **low-dimensional but not strictly 1D**  

---

## Phase Boundary: Model vs Reality

![Boundary comparison](figures/universality_boundary.png)

- White: effective-noise prediction  
- Red: true phase boundary  

The boundary curvature reveals structure not captured by 1D reductions.

---

## Physical Model

### Driven Two-Level System

H = (Ω/2) σ_x − Δ |r⟩⟨r|

### Two-Atom Interaction

H = Σ_i [(Ω/2) σ_x^(i) − Δ n_i] + V n₁ n₂

### Open-System Dynamics (Lindblad)

dρ/dt = −i[H, ρ] + Σ_k (L_k ρ L_k† − 1/2 {{L_k† L_k, ρ}})

Noise channels:
- spontaneous emission (γ)
- dephasing (γ_φ)

---

## Workflows

- Parameter sweeps over (Ω, Δ, V, γ, γ_φ)
- Lindblad open-system simulation
- CZ gate construction and compensation
- Fidelity, coherence, leakage metrics
- Phase-boundary extraction
- Scaling-law discovery

---

## Repository Structure

rydberg-parameter-lab/
├── README.md
├── notebooks/
├── src/
├── figures/
└── environment.yml

---

## Installation

pip install -r requirements.txt

or

conda env create -f environment.yml
conda activate rydberg-parameter-lab

---

## Dependencies

- Python 3.10+
- NumPy
- SciPy
- Matplotlib
- QuTiP

---

## Research Direction

This project focuses on:

- identifying **structure in noisy quantum systems**  
- reducing high-dimensional parameter spaces  
- understanding **limits of effective models**  
- constructing **interpretable scaling laws**  

---

## License

MIT License


## Key Results

- Emergence of an **effective noise coordinate**: γ_eff = γ + λ·γ_φ  
- Identification of a **controlled breakdown** of 1D scaling at low T  
- Recovery via a **low-dimensional (2D) model** with near-perfect predictive accuracy  
- Extraction of a **curved phase boundary** not captured by linear effective-noise models  

---

## Overview

This project studies **noise-affected Rydberg CZ gates** and identifies **low-dimensional structure** in open-system quantum dynamics.

A central observation:

> System behavior approximately reduces from a 2D noise space  
> to a 1D effective coordinate, but this reduction fails in a  
> predictable regime and can be systematically repaired.

---

## Emergent Effective Noise Coordinate

![Effective noise collapse](figures/effective_noise_collapse.png)

Across a wide parameter range:

γ_eff = γ + λ·γ_φ

This defines a dominant direction in noise space governing system response.

---

## Breakdown of 1D Scaling

![1D failure](figures/1d_failure.png)

At low T:

- scaling curves fail to align  
- deviations are systematic  
- indicates missing structure beyond γ_eff  

---

## Low-Dimensional Model Recovery

![2D fit quality](figures/2d_fit_quality.png)

A simple 2D model restores accuracy:

- predicted vs true values align nearly perfectly  
- confirms system is **low-dimensional but not strictly 1D**  

---

## Phase Boundary: Model vs Reality

![Boundary comparison](figures/universality_boundary.png)

- White: effective-noise prediction  
- Red: true phase boundary  

The boundary curvature reveals structure not captured by 1D reductions.

---

## Physical Model

### Driven Two-Level System

H = (Ω/2) σ_x − Δ |r⟩⟨r|

### Two-Atom Interaction

H = Σ_i [(Ω/2) σ_x^(i) − Δ n_i] + V n₁ n₂

### Open-System Dynamics (Lindblad)

dρ/dt = −i[H, ρ] + Σ_k (L_k ρ L_k† − 1/2 {L_k† L_k, ρ})

Noise channels:
- spontaneous emission (γ)
- dephasing (γ_φ)

---

## Workflows

- Parameter sweeps over (Ω, Δ, V, γ, γ_φ)
- Lindblad open-system simulation
- CZ gate construction and compensation
- Fidelity, coherence, leakage metrics
- Phase-boundary extraction
- Scaling-law discovery

---

## Repository Structure

rydberg-parameter-lab/
├── README.md
├── notebooks/
├── src/
├── figures/
└── environment.yml

---

## Installation

pip install -r requirements.txt

or

conda env create -f environment.yml
conda activate rydberg-parameter-lab

---

## Dependencies

- Python 3.10+
- NumPy
- SciPy
- Matplotlib
- QuTiP

---

## Research Direction

This project focuses on:

- identifying **structure in noisy quantum systems**  
- reducing high-dimensional parameter spaces  
- understanding **limits of effective models**  
- constructing **interpretable scaling laws**  

---

## License

MIT License
