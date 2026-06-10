# fsae-chassis-fea

Summary

Bio-inspired Formula Student spaceframe chassis designed in SolidWorks 2024 and evaluated via FEA in ANSYS Mechanical 2024 R2. Achieved 47.4% torsional stiffness improvement through targeted triangulation. Design concept derived from peregrine falcon skeletal mechanics.

# Bio-Inspired Formula Student Spaceframe Chassis — Design & FEA
**BEng Dissertation — Queen Mary University of London | April 2026**

> Supervisor: Dr Saqib Jivani | Module: EMS690U

## Overview

Designed, modelled, and evaluated a bio-inspired Formula Student (FSAE) tubular spaceframe chassis in SolidWorks 2024, with torsional stiffness analysis conducted in ANSYS Mechanical 2024 R2. The bio-inspired concept draws from the structural characteristics of the peregrine falcon, whose shoulder girdle exhibits significantly elevated bone mass and second moment of area as an adaptation to high-speed dive loading.

This principle was applied by designating the front and rear suspension hardpoint regions as reinforced shoulder zones — higher member density, increased wall thickness, and denser triangulation concentrated at force entry points — while simplifying geometry progressively away from these zones to minimise mass.

## Key Result

> **47.4% torsional stiffness improvement** (221.8 → 326.9 Nm/°) achieved through targeted triangulation optimisation at a mass cost of only 0.36 kg.

## Chassis Models Compared

| Parameter | Original Bio-Inspired | Optimised Bio-Inspired | Non-Bio-Inspired |
|---|---|---|---|
| Members | 40 | 44 | 44 |
| Max deformation (mm) | 7.3821 | 5.0078 | 5.4034 |
| Torsional stiffness (Nm/°) | 221.8 | **326.9** | 303.1 |
| Mass (kg) | 36.69 | 37.05 | 34.64 |
| K/m (Nm/°/kg) | 6.05 | **8.82** | 8.75 |
| Factor of safety | 16.9 | 19.5 | 18.7 |

The optimised bio-inspired model achieved a 7.9% absolute stiffness advantage over the geometrically identical non-bio-inspired control, confirming that localised reinforcement at suspension hardpoints produces measurable structural benefit beyond geometry alone.

## Bio-Inspired Design Concept

The peregrine falcon's shoulder girdle carries the highest bone mass and cross-sectional second moment of area of any comparable species — a structural adaptation to the large forces experienced during high-speed dives. Translated into a spaceframe:

- **Shoulder zones** (front and rear suspension hardpoints): 25.4 × 2.0 mm circular hollow section, dense triangulation, diagonals oriented to axial load paths
- **Mid-chassis, cockpit, front bulkhead**: 25.4 × 1.6 mm section, simplified geometry consistent with lower force magnitudes

## Material Selection

- **AISI 4130 chromoly steel** — yield strength 460–480 MPa, UTS 560–590 MPa
- Selected over aluminium alloys, titanium, and CFRP based on structural performance, weldability, cost, and end-of-life recyclability
- IMechE joint yield strength cap: 180 MPa for welded connections — joint strength governs structural calculations

## FEA Methodology

- **Software**: ANSYS Mechanical 2024 R2, static structural
- **Mesh**: Curvature-based, 3.0 mm global element size; 935,854 elements, 3,407,705 nodes
- **Mesh convergence**: Verified at 3.0 mm vs 2.5 mm — deformation change < 0.13%
- **Boundary conditions**: Fixed support at rear top corner edges; 1,500 N force couple at front suspension hardpoints generating 375 Nm applied torque
- **Stiffness calculation**: K = T/θ where θ = arctan(δ/d), d = 250 mm moment arm

## Regulatory Compliance

- Wheelbase: 1,575 mm (minimum 1,525 mm per T2.7.1)
- Front bulkhead width: 374 mm (below 400 mm threshold per T3.17.8)
- Main hoop brace attachment: within 160 mm of apex (per T3.10.3)
- Shoulder harness bar: 550 mm below hoop top (per T5.5.5)

## Tools Used

- SolidWorks 2024
- ANSYS Mechanical 2024 R2
- Ansys Granta EduPack

## Limitations & Future Work

- Single static torsional load case only — dynamic, braking, and combined loading not evaluated
- Rigid joint assumption overestimates physical stiffness (HAZ compliance excluded)
- Physical torsion testing recommended for FEA calibration
- Further triangulation iterations targeting cockpit and mid-chassis lateral faces would yield continued stiffness improvementsption overestimates physical stiffness (HAZ compliance excluded)
Physical torsion testing recommended for FEA calibration
Further triangulation iterations targeting cockpit and mid-chassis lateral faces would yield continued stiffness improvements
