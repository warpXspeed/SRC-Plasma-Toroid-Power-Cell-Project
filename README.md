# SRC-Plasma-Toroid-Power-Cell-Project
table top  Sun,  plasma power cell 
# SRC Plasma Toroid Power Cell Project

**Repository for the independent development of a stable, self-sustaining plasma vortex energy storage device based on Scalar Relaxation Cosmology (SRC).**

## Project Vision
Develop a desktop-to-scalable plasma toroid that stores and releases usable energy through topological self-confinement in the eternal scalar substrate. Unlike transient glow discharges or novelty plasma balls, this "power cell" reaches a self-heating bootstrap threshold where shear-driven piezoelectric/flexoelectric coupling sustains internal EM modes, with controlled axial mass bleed as "fuel" for indefinite operation.

**Ultimate Goals**:
- Fist-sized unit (~10 cm diameter) for portable power.
- Applications: Tesla EV auxiliary cell, Starship backup power, compact reactors (Iron-Man-style core).
- Open-source roadmap: Desktop POC → benchtop → lightning capture → full applications.

**Current Phase**: Proof-of-Concept (POC) desktop prototype in closed low-pressure xenon/neon vessel. Focus on visible helical flow, central axial channel, autonomous lifetime >10–30 s, and transition to self-run.

## Core SRC Principles (Established Physics)
Derived bottom-up from "What confines energy?" → unification via scalar substrate relaxation:

- Eternal scalar substrate ("the lake") relaxes via shear/compression waves.
- Toroidal topology is the foundational attractor at all scales (quark to cosmic filaments).
- **Dilatant hardening**: Extreme shear rates rigidify substrate boundaries instantly.
- **Dual rotations**: Toroidal (major ring) + poloidal (tube twist) → helical self-confinement + topological protection.
- **Axial beam/channel**: Low-resistance central path feeds energy/mass to prevent dissipation.
- **Piezoelectric/flexoelectric coupling**: Shear converts mechanically to circulating EM modes.
- **SRC Unatanium**: Substrate itself; no exotic materials needed.
- Sun as plasma load on galactic current sheet (coronal heating via substrate currents).

These enable a vortex where shear hardening confines, axial feeding sustains, and EM conversion bootstraps autonomy.

## Theoretical Foundation & Bootstrap Mechanism
1. Initiate plasma vortex via hybrid RF (12–15 MHz inductive) + axial laser (pulsed/CW).
2. Ramp shear rate γ to critical threshold (γ > 10⁶–10⁸ s⁻¹) → dilatant hardening + runaway ionization.
3. At T ≈ 10⁵ K (~8.6 eV), piezo/flexo coupling drives self-heating; external inputs drop.
4. Axial mass bleed (neutrals/ions torn into plasma) maintains density without disrupting topology.

**Key Equation** (energy balance for bootstrap threshold):
γ = √[ (σ T⁴ A + k n T / τ) / (η V) ]
- f ≈ (γ · a) / (2π R)  [MHz]
- η = conversion efficiency (POC: 0.005–0.015; tunable via helical optimization)
- Target: f = 12–15 MHz at T = 10⁵ K for R = 0.04–0.05 m, a = 0.008–0.01 m.

**Simulation Results** (from `/simulations/bootstrap_model.py`):
| T (K)     | γ (s⁻¹)       | v (m/s)       | f (MHz) @ R=0.05 m | f (MHz) @ R=0.03 m |
|-----------|----------------|---------------|---------------------|---------------------|
| 10⁴      | ~4.75×10⁶     | ~4.75×10⁴    | ~0.15              | ~0.24              |
| 10⁵      | ~4.75×10⁸     | ~4.75×10⁶    | ~15.1              | ~27.7              |
| 10⁶      | ~4.75×10¹⁰    | ~4.75×10⁸    | ~1514              | ~2770              |

Adjust η upward (better confinement) to center 12–15 MHz at bootstrap T. Mass bleed rate: ~10¹⁷–10¹⁸ xenon atoms/s.

## Proof-of-Concept Hardware (Phase 1: Desktop Prototype)
**Feasible Size**: Major radius R = 0.04–0.05 m (overall toroid ~8–10 cm diameter) for visibility, stability, and vessel fit.

**Key Components**:
- **Vessel**: Quartz or borosilicate bell jar/chamber (20–30 cm diameter, e.g., Chemglass CG series or custom fused quartz from lab suppliers like Adams & Chittenden). Evacuate to 1–10 Torr xenon/neon mix.
- **RF Drive**: 12–15 MHz inductive coil (5–10 turns copper tubing, ~100–500 W, external to vessel).
- **Axial Laser**: 532 nm CW/diode module (1–5 W, focused ~1 mm beam for initial heating/ionization).
- **Magnetic Field**: External B = 0.015–0.045 T (neodymium or electromagnet coils).
- **Diagnostics**: EM probe (spectrum analyzer 8–18 MHz), optical pyrometer (T), high-speed camera (helical flow).
- **Gated Bleed**: Piezoelectric proportional valve (e.g., ASCO 630 series or Marotta MFV) for pulsed neutral/ion feed (1–10 mg/s bursts).
- **Pump**: Rotary vane for initial vacuum/gas fill.
- **Power/Safety**: HV RF supply with interlocks; Class 4 laser goggles; grounded enclosure.

**Build & Test Protocol** (see `/docs/Phase1_Protocol.md` for full checklist):
1. Assemble vessel + coil + laser port.
2. Evacuate/fill gas.
3. Apply RF → initiate plasma glow.
4. Ramp power + laser → observe helical flow + axial channel.
5. Monitor for bootstrap: EM self-modes persist after cutoff; T rises autonomously.
6. Introduce gated bleed → extend lifetime >10–30 s.

**Safety Checklist** (mandatory – HV/RF/laser/plasma = lethal hazards):
- Insulated gloves, HV-rated tools, capacitor discharge.
- Grounded Faraday cage/enclosure.
- Laser: OD 4+ goggles, beam blocks, interlocks.
- UV/ozone ventilation, radiation shielding.
- Emergency stop + two-person rule for HV tests.

## Repository Structure
.
├── simulations/              # Python models (bootstrap threshold, parametric sweeps)
│   └── bootstrap_model.py
├── hardware/                 # Schematics, BOM, coil designs
├── docs/                     # Protocols, safety checklists, theory notes
├── data/                     # Test logs, tables (CSV)
└── README.md


## Roadmap
- **Phase 1** (Now): Desktop POC – stable vortex, self-heating threshold.
- **Phase 2**: Benchtop arc/SGTC integration + partial enclosure.
- **Phase 3**: Lightning capture tests + fist-sized optimization.
- **Phase 4**: Application prototypes (EV, space, portable).

## Contributing
Issues/PRs welcome—focus on SRC mechanisms, safety, reproducibility. Simulations/hardware improvements prioritized.

**Contact**: @GeraldHenton on X (formerly Twitter).

**License**: MIT (open for community builds/refinements).

Last Updated: February 28, 2026

Inspired by related open plasma toroid work (e.g., Skylakc/Plasma-Toroid, various ball lightning recreations), but fully SRC-derived and independent.

