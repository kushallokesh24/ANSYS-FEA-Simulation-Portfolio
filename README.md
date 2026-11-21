# ANSYS R17.0 — Structural, Thermal & Harmonic FEA Simulation Portfolio

**Author:** Kushal L (`@kushallokesh24` | `@kushaldeaignme`)  
**Institution:** Department of Mechanical Engineering, Malnad College of Engineering, Hassan  
**Portfolio Website:** [https://github.io](@kushallokesh24`)

---

## Overview
A collection of Finite Element Analysis (FEA) simulations conducted in **ANSYS R17.0 (Mechanical APDL)** covering 2D structural stress concentration, truss and beam mechanics, steady-state thermal conduction, and harmonic frequency response.

## Simulation Case Studies

### 1. Static Structural Stress Concentration — Plate with Central Hole
- **Analysis Type:** 2D Plane Stress Static Structural Analysis
- **Key Outputs:** Maximum Von Mises Stress (`SEQV = 6923.79`), Maximum Displacement (`DMX = 2.46549`), and Nodal Reaction Forces (`FX = 2.00E+06`).
- **Engineering Insight:** Evaluated stress distribution around a central circular discontinuity under uniaxial tension and verified equilibrium reaction loads.

### 2. 2D Truss Structural Analysis (`LINK180`)
- **Analysis Type:** Linear Static Truss Analysis
- **Key Outputs:** Axial Member Stresses (`MAX = +400.00` tension, `MIN = -429.13` compression), Nodal Displacements (`UX_max = 2.0000`), and Support Reactions.

### 3. Beam Bending Moment & Shear Force Analysis (`SMIS3 / SMIS6`)
- **Analysis Type:** 1D Structural Beam Bending & Shear Analysis
- **Key Outputs:** Bending Moment (`SMIS3/SMIS16`), Shear Force (`SMIS6/SMIS19`), and Support Reaction Forces/Moments (`FY`, `MZ`).

### 4. 1D Steady-State Thermal Conduction Analysis
- **Analysis Type:** Steady-State Thermal Conduction (`TEMP`)
- **Key Outputs:** Nodal Temperature Gradient (`303 K` to `1073 K`) and Element Heat Flow (`478.74`).

### 5. Harmonic Vibration & Frequency Response Analysis (`POST26`)
- **Analysis Type:** Harmonic Sweep Frequency Response (`UX_2`, `UY_2` Amplitude & Phase)
- **Key Outputs:** Identified resonant frequency peaks (`~1400 Hz` & `~4050 Hz` in lateral mode; `~50 Hz` & `~290 Hz` in vertical mode) and `180°` phase shift across resonance.

---

## Files Included
- `ANSYS_FEA_Simulation_Report.pdf` — Compiled ANSYS R17.0 contour plots, frequency response graphs, and nodal/element solution listings.
