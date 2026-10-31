[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23835274.svg)](https://doi.org/10.5281/zenodo.23835274)

Overview

This repository contains the computational code, simulation scripts, and diagnostic notebooks for simulating the 1+1-dimensional Schwinger model (Quantum Electrodynamics) on a quantum processor emulator. The project investigates real-time vacuum decay and electron-positron pair production under extreme laser electric field quenches, utilizing parameters chosen to align with high-field physics regimes studied at facilities like the Extreme Light Infrastructure - Nuclear Physics (ELI-NP) project.

Repository Contents

The core material is contained within a self-contained Jupyter Notebook designed as a computational essay that links theoretical derivations directly to code execution. The pipeline covers:

Lattice Hamiltonian Construction: Setting up the $N=6$ site Kogut-Susskind staggered fermion model via Jordan-Wigner transformation and native SparsePauliOp arithmetic.

Laser Quench Evolution: Implementing a time-dependent Gaussian-envelope oscillating electric field coupled via site-dependent driving operators, evolved using first-order Suzuki-Trotter decomposition (PauliEvolutionGate).

NISQ Noise Modeling & ZNE Mitigation: Executing noisy density matrix simulations via Qiskit Aer (AerSimulator) under a standard depolarizing noise model ($\epsilon_{1\text{q}} = 0.002$, $\epsilon_{2\text{q}} = 0.015$), followed by Zero-Noise Extrapolation using scale-factor circuit folding ($sf \in \{1, 3\}$) and linear fitting.

Advanced Quantum Diagnostics: Tracking the growth of Von Neumann entanglement entropy across a spatial bipartition as a proxy for string breaking, alongside spatiotemporal heatmaps mapping site-resolved chiral condensate melting ($\langle \bar{\psi}\psi \rangle_i$).

Software Requirements & Dependencies

To run the simulation and generate the diagnostic figures, the code requires Python along with the following libraries:

qiskit

qiskit-aer

numpy

matplotlib
