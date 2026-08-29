# Modeling of a Grid-Connected Converter Realized Using a Single-Phase H-Bridge

This folder contains the simulation notebook for studying a single-phase grid-connected converter realized using an H-bridge (full bridge) with two switching poles.

The simulation file is intended for understanding the operating principle and behavior of the converter model. It is not a substitute for detailed converter design validation.

The material is organized for course use. It follows the earlier folder on the single switching pole, and the notebooks are parameterized so that the two studies can be compared directly.

## Aim

The aim of this notebook is to help learners analyze how the modulation scheme, converter parameters, and model assumptions influence:

- AC-side current injection into the grid
- Converter output voltage `v_{ab}(t)` and its switching levels
- Individual switch currents and rail-current distribution
- Harmonic content and total harmonic distortion (THD)

## Model in This Folder

1. `H-Bridge-Ideal.ipynb`
   - Ideal constant and balanced DC-link assumption
   - Single-state model focused on filter current dynamics
   - Bipolar and unipolar PWM, selectable through `pwm_mode`
   - Suitable for learning switching-function generation, waveform-level behavior, switch-current distribution, and harmonic analysis

## Analyses You Can Perform

Using the current notebook, users can perform the following analyses:

- Define and compare PWM carriers and the two leg switching functions
- Compare bipolar and unipolar modulation, and their effect on the levels of `v_{ab}(t)`
- Simulate converter waveforms in time domain
- Inspect injected current `i_f(t)` and converter output voltage `v_{ab}(t)`
- Reproduce the switch-current table for the four switching combinations and plot `i_a^+`, `i_a^-`, `i_b^+`, `i_b^-`
- Compute and visualize top-rail and bottom-rail currents, and verify that they are equal
- Evaluate harmonic spectra (magnitude and phase)
- Compute THD of the converter output voltage and injected current, and verify how unipolar switching shifts the first sideband cluster

## Notes on Parameter Scaling

The H-bridge applies `v_{ab}` across the filter, whose fundamental peak is `M*Vdc`, twice that of a single switching pole. The DC-link voltage is therefore set to 350 V here, against 700 V in the switching-pole folder, so that both studies operate at the same AC-side point.

## Software Requirements

- Python 3.10 or newer
- `numpy`
- `scipy`
- `matplotlib`
- `jupyter`

Install dependencies with:

```bash
pip install numpy scipy matplotlib jupyter
```

## How to Run

1. Create and activate a Python virtual environment.
2. Install the required packages.
3. Start Jupyter and open the notebook.
4. Run cells from top to bottom.

## Notes

- This notebook is the reference notebook for waveform, switch-current, and harmonic analysis of the H-bridge.
- The DC link is assumed constant and balanced throughout, so DC-link dynamics are outside the scope of this notebook.
- The notebook is designed for educational study of H-bridge converter behavior and interpretation.

## Credits

Simulation ideas, modeling approach, and technical interpretation are by the author.
AI assistance was used only to polish code structure and documentation language.
