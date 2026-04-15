![Rydberg Parameter Lab](figures/banner.png)

# Rydberg Parameter Lab

**Open-system modeling of neutral-atom CZ gates using Lindblad dynamics, with direct connections to QCVV and noise characterization.**

---

## Key Contributions

- Modeled CZ gate dynamics under open-system noise (Lindblad master equation)
- Introduced an effective noise coordinate (γ_eff) to capture combined decoherence effects
- Identified scaling behavior and phase boundaries in noisy gate regimes
- Generated parameter sweeps over Ω, Δ, V, γ → fidelity landscapes
- Connected noise models to QCVV-style benchmarking and gate characterization

---

## Overview

This repository explores how **noise and control parameters shape fidelity in neutral-atom quantum gates**, with a focus on:

- decoherence (γ, γ_φ)
- gate depth dependence
- deviations from simple exponential decay
- structure in noisy quantum dynamics

---

## Example Behavior

![Fidelity decay and CZ interaction](figures/hero_figure.png)

*Example: fidelity decay under increasing gate depth, with interaction parameters (Ω, Δ, V) governing dynamics.*

---

## 🚀 QuickStart

Explore the full pipeline interactively:

[![Open Notebook 58 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thinkthoughts/rydberg-parameter-lab/blob/main/notebooks/58_lindblad_to_gamma_pipeline.ipynb)

**Jump to the physics result (blockade transition):**

[![Open Notebook 63 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thinkthoughts/rydberg-parameter-lab/blob/main/notebooks/63_blockade_boundary_transition.ipynb)

---

### Suggested progression

- Notebook 58 — Lindblad → Γ(x) → S(x)  
- Notebook 59–61 — universality phase diagrams  
- Notebook 62 — labeled regimes  
- Notebook 63 — blockade transition  

---

## Key Results

- Effective noise coordinate: γ_eff = γ + λ·γ_φ  
- Breakdown of 1D scaling  
- Recovery via structured Γ(x)  
- Stretched-exponential universality  
- Local exponent field b_local(x)  
- Global exponent as projection  
- Sensitivity-derived projection weight  

---

## Overview

Dynamics are governed by a **structured, scale-dependent rate process Γ(x)**.

![Theory summary](figures/theory_figure.png)

---

## Stretched-Exponential Universal Law

![Final universal law](figures/stretched_exponential_fit.png)

S(x) ≈ exp(−a x^b)

---

## Universality Phase Diagrams

![Phase diagram](figures/phase_diagram_b.png)
![Ratio phase diagram](figures/ratio_phase_diagram.png)

b = f(physical parameters)

---

## Functional Universality

![Functional universality](figures/functional_universality_map.png)

b = Functional[Γ_eff(x)]

---

## Learned Mapping

![Learned universality](figures/learned_universality_map.png)

b ≈ LearnedModel[Γ_eff(x)]

---

## Analytic Approximation

![Analytic b prediction](figures/analytic_b_prediction.png)

---

## Local Exponent Field

![Local exponent field](figures/local_exponent_fields.png)

b_local(x) = x Γ(x) / ∫ Γ

---

## Global Exponent as Projection

![Projection comparison](figures/projection_comparison.png)

b ≈ ∫ w(x) b_local(x) dx  

---

## Sensitivity-Derived Projection Weight

![Sensitivity weight](figures/sensitivity_weight_derivation.png)

w(x) ∝ |∂ log S(x) / ∂ b|

---

## Blockade Boundary and Universality Transition

![Blockade transition](figures/blockade_transition_b.png)
![Blockade sensitivity](figures/blockade_sensitivity.png)

V / Ω ≈ 1 marks the Rydberg blockade onset.

![Decay curves](figures/blockade_decay_curves.png)
![Gamma deformation](figures/blockade_gamma.png)
![Local exponent](figures/blockade_blocal.png)
![Fit quality](figures/blockade_fit_quality.png)

---

## Interpretation

The exponent **b acts as a detector of many-body constraint onset**.

Hierarchy:

V / Ω  
→ Γ(x) deformation  
→ b_local(x) deformation  
→ global exponent shift  

---

## Physical Model

H = (Ω/2) σ_x − Δ |r⟩⟨r|  

H = Σ_i [(Ω/2) σ_x^(i) − Δ n_i] + V n₁ n₂  

dρ/dt = −i[H, ρ] + Σ_k (L_k ρ L_k† − ½ {L_k† L_k, ρ})

---

## Installation

pip install -r requirements.txt  

---

## License

MIT License
