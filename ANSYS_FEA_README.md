# ANSYS R17.0 Finite Element Analysis (FEA) Simulation Portfolio

**Author:** Kushal L (`@kushallokesh24` / `@kushaldeaignme`)  
**Institution:** Department of Mechanical Engineering, Malnad College of Engineering, Hassan  
**Software:** ANSYS Mechanical APDL R17.0  

---

## Overview
A collection of structural, thermal, and harmonic dynamic Finite Element Analysis (FEA) simulations conducted in **ANSYS R17.0**, covering stress concentration, truss and beam mechanics, steady-state heat conduction, and frequency-response vibration analysis.

---

## 1. Stress Concentration Analysis — Plate with Central Hole (2D Structural)
* **Element & Solution Type:** 2D Planar Structural Element | Static Nodal & Element Solution
* **Loading & Boundary Conditions:** Uniaxial tensile load (`FX = 2.00E+06` total reaction) with constrained support nodes.
* **Key Results:**
  * **Maximum Displacement (`DMX`):** `2.46549`
  * **Maximum Von Mises Stress (`SEQV`):** `6923.79` (concentrated at the top and bottom edges of the central circular cutout)
  * **Minimum Von Mises Stress (`SMN`):** `516.569`

---

## 2. 2D Truss Structural Analysis (`LINK180`)
* **Element Type:** `LINK180` (3D Spar / Truss Element)
* **Loading & Reactions:** External loads (`FX = -4000.0`, `FY = 5000.0`) supported at pinned/roller nodes.
* **Key Results:**
  * **Peak Tensile Axial Stress (`SX`):** `+400.00` (Element 1)
  * **Peak Compressive Axial Stress (`SX`):** `-429.13` (Element 2)
  * **Maximum Nodal Displacement (`UX`):** `2.0000` at Node 2

---

## 3. Beam Bending Moment & Shear Force Analysis (`SMIS3 / SMIS6`)
* **Element & Solution Type:** 1D Structural Beam Elements (`SMIS3/SMIS16` Bending Moment, `SMIS6/SMIS19` Shear Force)
* **Key Results:**
  * **Multi-Span / Stepped Load Case:** Bending stress/moment range from `-1552.32` (Elem 40) to `+1492.07` (Elem 41); Shear range from `-1045.50` to `+765.17` (`FY` total reaction `1810.7`).
  * **Point & Distributed Load Case:** Maximum bending line stress `3371.05` (Elem 50), shear range `-1601.0` to `+3401.0` (`FY` total reaction `5002.0`).
  * **Cantilever Beam Case:** Peak bending magnitude `-287.5` at fixed root (Elem 1), reaction `FY = 50.0`, `MZ = 290.0`.

---

## 4. 1D Steady-State Heat Conduction Analysis (`HEAT` / `TEMP`)
* **Analysis Type:** Steady-State Thermal Conduction across composite/multi-node wall layers.
* **Key Results:**
  * **Case A (Furnace Wall Gradient):** Temperature drops from `600.00` (Node 1) through `418.18` and `527.27` to `200.00` (Node 4).
  * **Case B (High-Temperature Composite Wall):** Nodal temperatures from `1073.0` (Node 1) -> `1071.4` -> `1055.4` -> `656.49` -> `306.19` -> `303.00` (Node 6) with steady-state element heat flow `478.74`.

---

## 5. Harmonic Vibration & Frequency Response Analysis (`POST26`)
* **Analysis Type:** Harmonic Response Analysis (`UX_2` and `UY_2` amplitude & phase angle across frequency sweeps).
* **Key Results:**
  * **High-Frequency Sweep (`0 - 5000 Hz`):** Identified two primary resonance peaks near `~1450 Hz` (`UX_2` amplitude `~2.1E-04`) and `~4050 Hz` (`~1.7E-04`) with a `180 deg` phase shift across resonance.
  * **Low-Frequency Sweep (`0 - 400 Hz`):** Identified fundamental resonance peak near `~48-50 Hz` (`UY_2` amplitude `~0.52`) and secondary mode near `~290 Hz`.
