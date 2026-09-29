# Two-State Time Evolution

An interactive, single-page simulation for teaching the time dependence of a quantum system with two non-degenerate energy levels: phase, angular frequency, relative phase, and why only the relative phase can be measured.

**Run it in your browser:** https://lengelhardt.github.io/two-state-time-evolution/

Nothing to install. To run it offline, download `index.html` and open it in any modern browser. An internet connection is only needed for the web fonts.

## What it shows

The state evolves as

|ψ(t)⟩ = c₁ e^(−iE₁t/ħ) |E₁⟩ + c₂ e^(−iE₂t/ħ) |E₂⟩

This form assumes a **time-independent Hamiltonian**: H, its eigenstates and its eigenvalues stay fixed while the state evolves. Changing the energies or eigenstates defines a new H and restarts the clock at t = 0.

For a spin, a toggle at the top of DEFINE HAMILTONIAN switches from **ENERGIES** (static H, the default) to **MAGNETIC FIELD**, an optional mode that sets H with a static field B₀ in tesla, for an electron, proton or neutron. In that mode an **oscillating drive** B₁cos(ωt) perpendicular to B₀ makes H time dependent: **magnetic resonance**, following L. Engelhardt, *Am. J. Phys.* **83**, 1051 (2015). The Schrödinger equation is then integrated numerically, with exactly unitary steps; because H(t) repeats every drive period, one period is enough to reach any time. On resonance the spin spirals from |+⟩z to |−⟩z in the flip time τ = 2π/Ω, with Ω = γB₁. An **illustrative** range uses strong drives (Ω/ω₀ ≈ 0.1) so the spiral and the small wiggles are visible; a **realistic** range uses laboratory strengths (1 μT to 1 mT), where a flip takes thousands to millions of Larmor turns, and shows the state with a strobe synchronized to the drive and the fast precession as a blur.

The simulation lets students watch this from four angles, one to four at a time (it starts with two: rotating phasors and measurement probabilities):

- **Rotating phasors:** each coefficient is an arrow in the complex plane turning at its own angular frequency ω = E/ħ (clockwise for E > 0).
- **Relative phase:** the same motion with the global phase e^(−iω₁t) factored out. c₁ stands still and c₂ turns at ω₂ − ω₁.
- **Bloch sphere:** the state precesses about the energy axis at ω₂₁; the latitude (the energy probabilities) never changes.
- **Measurement probabilities:** P(+) and P(−) in a chosen measurement basis, traced out as time runs. They oscillate at the Bohr frequency ω₂₁ unless you measure in the energy basis.

## Controls

- **Initial state:** |±⟩ along z, x or y, any direction (θ, φ), or |c₂| and φ₂ directly. The state is written in the z basis with the |+⟩z coefficient real and non-negative.
- **Measurement basis:** z, x, y or any direction n.
- **Define Hamiltonian:** energy eigenstates |±⟩ along z (default), x, y or n; energies E₁ and E₂ set by slider or by dragging the lines in the level diagram; the Hamiltonian as a 2×2 matrix in any of those bases.
- **Magnetic-field mode (spin only, optional):** an electron, proton or neutron in a static field B₀ (tesla, or the Larmor frequency ω₀ = γB₀), plus an oscillating drive: on/off, illustrative or realistic range, strength B₁, frequency ω (or the detuning), and a button to tune to resonance. Switching back to ENERGIES restores E₁ and E₂.
- **Time:** play/pause (or the space bar), step, and jump ahead by exactly one period T₁, T₂ or T₂₁, or (driven) by one flip time τ.
- **System:** Spin ½ (default) or Qubit. The math is identical; qubit mode relabels |±⟩z, |±⟩x, |±⟩y as |0⟩/|1⟩, |±⟩, |±i⟩, uses 0/1 indices, and defaults to a 5 GHz qubit.
- **Units:** physical units (default: eV and fs for a spin, μeV and ns for a qubit and in magnetic-field mode; ħ = 0.658 in all of them) or dimensionless ħ = 1.
- **Reset to defaults:** one button (click twice) restores every setting; full screen, the presentation tools and the system choice are kept.
- **Presentation tools:** full screen, a laser pointer and a markerboard for drawing over the screen.

The **INFO** button inside the simulation has the physics, a full control reference and a list of things to try in class.

## Credits and license

Created by Larry Engelhardt, Francis Marion University, with Claude (Anthropic), 2026.

The layout, styling and presentation tools are adapted from the *Electric Charge Simulator* v7.02 by Mehmet Fatih Tasar, Georgia State University, which is licensed under CC BY-NC-SA 4.0.

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). See [LICENSE](LICENSE).
