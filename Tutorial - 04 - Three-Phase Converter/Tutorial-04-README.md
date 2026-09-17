# Tutorial 04 — Three-Phase Converter

## Notebooks

| Notebook | Description |
| -------- | ----------- |
| `Three-Phase-CSVPWM-Ideal.ipynb` | Switched model of a three-phase converter with ideal (constant) DC link, using carrier-based Conventional Space Vector PWM (CSVPWM). |

## What Is Covered

- Instantaneous switching model of a Y-connected three-phase voltage-source converter.
- Carrier-based CSVPWM implementation using min-max (common-mode) offset injection.
- Time-domain waveforms: filter currents, pole voltages, phase voltages, DC-side current.
- Overlay of grid-injected currents with grid voltages to visualize the phase relationship.
- Harmonic analysis (DFT) and THD computation for the pole voltage and injected current.
- Option to switch between CSVPWM and plain SPWM for comparison.

## How to Run

```
pip install numpy scipy matplotlib jupyter
jupyter notebook Three-Phase-CSVPWM-Ideal.ipynb
```
