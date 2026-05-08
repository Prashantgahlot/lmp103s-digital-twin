# LMP-103S Green Propellant Combustion Digital Twin

A physics-based Digital Twin framework for real-time fault detection 
in LMP-103S (ADN-based) green propellant bipropellant combustion systems.

**Author:** Prashant Gahlot  
**Affiliation:** MSc Aerospace Engineering, University of Bologna  
**Status:** Active research — extending MSc thesis on green propellant 
optimisation for deep-space missions

---

## Overview

This repository implements a two-paper research programme:

**Paper 1 (submitted — Acta Astronautica, May 2026):**  
Thermochemical Performance Analysis of LMP-103S Green Propellant 
Bipropellant Combinations — quantifying ADN decomposition diluent 
penalties via Cantera equilibrium modelling.

**Paper 2 (in development):**  
Digital Twin framework for real-time combustion chamber health 
monitoring — integrating Cantera physics-based simulation with 
LSTM fault detection.

---

## Key Results

### Paper 1 — Thermochemical Analysis
- ADN decomposition diluents impose **18.2–34.6% Isp penalty** 
  depending on fuel type
- Ethanol/LMP-103S achieves **<1% Isp penalty at O/F=10** 
  (near-parity with pure O₂)
- Counter-intuitive density impulse advantage: ethanol/LMP-103S 
  **exceeds pure O₂ baseline by 6.8%** at high O/F ratios
- Monte Carlo uncertainty analysis: Isp CV = 2.08% (N=500)

### Paper 2 — Digital Twin & Fault Detection
- LSTM model: **99.54% accuracy**, AUC-ROC = 0.9998
- Detection delay: **0.6–1.5 seconds** from fault onset
- Three fault modes detected: catalyst degradation, O/F drift, 
  pressure oscillation
- Model size: **32,036 parameters** — suitable for embedded deployment

---

## Repository Structure
├── notebooks/
│   ├── Paper1_LMP103S_Thermochemical_Analysis.ipynb
│   └── Paper2_DigitalTwin_Combustion.ipynb
├── figures/
│   ├── Fig1_performance_comparison.png
│   ├── Fig2_diluent_penalty.png
│   ├── Fig3_pressure_effect.png
│   ├── Fig4_monte_carlo.png
│   ├── Fig5_mission_trade.png
│   └── dt_fig1-5_*.png
├── data/
│   └── combustion_dt_dataset.csv
└── README.md

---

## Technical Stack

- **Thermochemical modelling:** Cantera 3.2.0, GRI-Mech 3.0
- **ML framework:** TensorFlow/Keras 2.20
- **Scientific computing:** NumPy, SciPy, Pandas
- **Visualisation:** Matplotlib

---

## Citation

If you use this work, please cite:

Gahlot, P. (2026). "Thermochemical Performance Analysis of LMP-103S 
Green Propellant Bipropellant Combinations: Quantification of ADN 
Decomposition Diluent Penalties via Cantera Equilibrium Modelling." 
*Acta Astronautica* (under review).

---

## Contact

prashant.gahlot@studio.unibo.it  
[LinkedIn](https://linkedin.com/in/prashant-gahlot)  
AIAA Member No. 1749577

## Note on Data and Models
The full training dataset (65,000 samples) is included in `data/`.
The trained LSTM model weights are available on request due to file size constraints.

