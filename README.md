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
