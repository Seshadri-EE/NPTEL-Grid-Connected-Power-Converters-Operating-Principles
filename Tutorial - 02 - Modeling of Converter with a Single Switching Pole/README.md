# Modeling of a Grid-Connected Converter Realized Using a Switching Pole

This folder contains simulation notebooks for studying a single-phase grid-connected converter realized using a switching pole.

The simulation files are intended for understanding the operating principle and behavior of the converter models. They are not a substitute for detailed converter design validation.

The material is organized for course use, with a progression from an idealized model to more detailed models.

## Aim

The aim of these notebooks is to help learners analyze how PWM switching, converter parameters, and model assumptions influence:

- AC-side current injection into the grid
- Pole-voltage switching behavior
- Rail-current distribution
- Harmonic content and total harmonic distortion (THD)

## Models in This Folder

1. `Switching-Pole-Ideal.ipynb`
   - Ideal balanced DC-link assumption
   - Single-state model focused on filter current dynamics
   - Suitable for learning switching-function generation, waveform-level behavior, and harmonic analysis

2. `Switching-Pole-CurrentSource.ipynb`
   - Current-source-driven converter model with a prescribed DC-side source current
   - Extends the ideal case by including capacitor-voltage and DC-link dynamics

## Analyses You Can Perform

Using the current notebooks, users can perform the following analyses:

- Define and compare PWM carriers and switching functions
- Simulate converter waveforms in time domain
- Inspect injected current `i_f(t)` and pole voltage `v_{ao}(t)`
- Compute and visualize top-rail and bottom-rail currents
- Evaluate harmonic spectra (magnitude and phase)
- Compute THD of pole voltage and injected current

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
3. Start Jupyter and open the notebook of interest.
4. Run cells from top to bottom.

## Notes

- The ideal notebook is currently the reference notebook for waveform and harmonic analysis.
- The current-source notebook is the detailed model companion to the ideal notebook.
- Both notebooks are designed for educational study of switching-pole converter behavior and interpretation.

## Credits

Simulation ideas, modeling approach, and technical interpretation are by the author.
AI assistance was used only to polish code structure and documentation language.
