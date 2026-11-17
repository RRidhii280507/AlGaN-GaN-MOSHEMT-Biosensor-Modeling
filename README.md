# Analytical Modeling of AlGaN/GaN MOS-HEMT for Biosensor Applications

## Overview

This project investigates the analytical modeling and electrical characteristics of an AlGaN/GaN Metal-Oxide-Semiconductor High Electron Mobility Transistor (MOS-HEMT) for biosensing applications.

The device utilizes polarization-induced two-dimensional electron gas (2DEG) formation at the AlGaN/GaN heterointerface. A nanogap cavity introduced beneath the gate enables dielectric modulation when biomolecules occupy the sensing region, resulting in measurable variations in gate capacitance, threshold voltage, and drain current.

A physics-based analytical model was implemented in Python to reproduce the drain current versus gate voltage (ID–VG) characteristics for different biomolecules. The analytical results were compared against simulation data reported in the reference literature.

## Project Objectives

- Study the physical operating principles of AlGaN/GaN MOS-HEMT devices, including spontaneous and piezoelectric polarization.
- Investigate the formation and modulation of the 2DEG channel at the heterostructure interface.
- Develop an analytical model incorporating gate capacitance, carrier concentration, and drain-current behavior.
- Evaluate dielectric modulation caused by different biomolecules within the nanogap cavity.
- Compare analytical ID–VG characteristics with published simulation results.

## Device Structure

The investigated MOS-HEMT consists of an AlGaN/GaN heterostructure with a nanogap sensing cavity located beneath the gate electrode.

| Parameter | Value |
|---|---|
| Gate Length | 1 µm |
| Gate Width | 100 µm |
| AlGaN Barrier Thickness | 25 nm |
| GaN Buffer Thickness | 2 µm |
| Aluminum Mole Fraction | 0.3 |
| Nanogap Cavity Length | 500 nm |
| Nanogap Cavity Height | 20 nm |
| Source-to-Gate Spacing | 2.5 µm |
| Gate-to-Drain Spacing | 4.5 µm |

The structure incorporates a SiO₂-filled region and a biomolecule-sensitive nanogap cavity beneath the gate.

## Working Principle

### 1. Polarization-Induced 2DEG Formation

The AlGaN/GaN heterostructure exhibits spontaneous and piezoelectric polarization due to its crystal structure and lattice mismatch.

The polarization discontinuity at the interface produces fixed charges and leads to the formation of a high-density two-dimensional electron gas (2DEG), providing a conductive channel without conventional channel doping.

### 2. Dielectric Modulation

When biomolecules occupy the nanogap cavity, the effective dielectric constant beneath the gate changes.

This modifies the effective gate capacitance and influences the 2DEG carrier concentration, producing changes in the drain-current characteristics.

### 3. Electrical Detection

The device response is analyzed through:

- Drain current (ID)
- Gate voltage (VG)
- Threshold voltage shift (ΔVth)
- Drain-on-current sensitivity (SIon)

These parameters provide electrical indicators of changes in the sensing cavity.

## Analytical Modeling

The Python implementation evaluates the electrical behavior of the MOS-HEMT using analytical expressions for:

- Effective oxide and heterostructure capacitances
- 2DEG carrier concentration
- Source-side and drain-side carrier densities
- Drain current as a function of applied bias
- Sensitivity and threshold-voltage variation

The effective MOS-HEMT capacitance is modeled using:

1 / C_MOSHEMT = 1 / C_HEMT + 1 / C_ox

The drain-on-current sensitivity is defined as:

SIon = [Ion(with biomolecule) − Ion(without biomolecule)] / Ion(without biomolecule)

The analytical formulation follows the device model discussed in the referenced research literature.

## Biomolecules Investigated

Four biomolecule cases were considered:

| Biomolecule | Approximate Dielectric Constant |
|---|---:|
| Uricase | 1.54 |
| Streptavidin | 2.10 |
| Protein | 2.50 |
| Cholesterol Oxidase (ChOx) | 3.50 |

Each biomolecule changes the effective dielectric environment beneath the gate, resulting in different drain-current responses.

## Results and Observations

The analytical model was implemented in Python and evaluated for a drain voltage of 5 V.

ID–VG characteristics were generated for Protein, ChOx, Uricase, and Streptavidin, and compared with published simulation data.

### Key Observations

- The analytical characteristics reproduced the overall trends observed in the reference simulation data.
- Introducing biomolecules into the cavity modified the drain-current characteristics through dielectric modulation.
- The device exhibited sensitivity to variations in the dielectric properties of the cavity.
- The project investigated threshold-voltage shifts and drain-current sensitivity as electrical sensing metrics.

The referenced study reported a notable uricase response, including a threshold-voltage shift of approximately 1.055 V under its investigated conditions.

## Tools and Technologies

- **Python:** Numerical implementation and analytical calculations
- **NumPy:** Numerical computation
- **Matplotlib:** Electrical characteristic visualization
- **Semiconductor Device Physics:** Heterostructures, polarization, 2DEG formation
- **Analytical Modeling:** Capacitance, carrier concentration, drain-current characteristics


