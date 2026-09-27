# Two-State Time Evolution

An interactive, single-page simulation for teaching the time dependence of a quantum system with two non-degenerate energy levels: phase, angular frequency, relative phase, and why only the relative phase can be measured.

**Run it in your browser:** https://lengelhardt.github.io/two-state-time-evolution/

Nothing to install. To run it offline, download `index.html` and open it in any modern browser. An internet connection is only needed for the web fonts.

## What it shows

The state evolves as

|ψ(t)⟩ = c₁ e^(−iE₁t/ħ) |E₁⟩ + c₂ e^(−iE₂t/ħ) |E₂⟩

This form assumes a **time-independent Hamiltonian**, and this version of the simulation is limited to that case: H, its eigenstates and its eigenvalues stay fixed while the state evolves. Changing the energies or eigenstates defines a new H and restarts the clock at t = 0.

The simulation lets students watch this from four angles, one to four at a time:

- **Rotating phasors:** each coefficient is an arrow in the complex plane turning at its own angular frequency ω = E/ħ (clockwise for E > 0).
- **Relative phase:** the same motion with the global phase e^(−iω₁t) factored out. c₁ stands still and c₂ turns at ω₂ − ω₁.
- **Bloch sphere:** the state precesses about the energy axis at ω₂₁; the latitude (the energy probabilities) never changes.
- **Measurement probabilities:** P(+) and P(−) in a chosen measurement basis, traced out as time runs. They oscillate at the Bohr frequency ω₂₁ unless you measure in the energy basis.

## Controls

- **Initial state:** |±⟩ along z, x or y, any direction (θ, φ), or |c₂| and φ₂ directly. The state is written in the z basis with the |+⟩z coefficient real and non-negative.
- **Measurement basis:** z, x, y or any direction n.
- **Define Hamiltonian:** energy eigenstates |±⟩ along z (default), x, y or n; energies E₁ and E₂ set by slider or by dragging the lines in the level diagram; the Hamiltonian as a 2×2 matrix in any of those bases.
- **Time:** play/pause (or the space bar), step, and jump ahead by exactly one period T₁, T₂ or T₂₁.
- **Units:** eV and fs (default, ħ = 0.658 eV·fs) or dimensionless ħ = 1.
- **Presentation tools:** full screen, a laser pointer and a markerboard for drawing over the screen.

The **INFO** button inside the simulation has the physics, a full control reference and a list of things to try in class.

## Credits and license

Created by Larry Engelhardt, Francis Marion University, with Claude (Anthropic), 2026.

The layout, styling and presentation tools are adapted from the *Electric Charge Simulator* v7.02 by Mehmet Fatih Tasar, Georgia State University, which is licensed under CC BY-NC-SA 4.0.

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). See [LICENSE](LICENSE).
