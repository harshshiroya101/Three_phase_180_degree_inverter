# Three-Phase 180-Degree Inverter

## Overview
This project contains a MATLAB/Simulink model (`Three_phase_180_degree_inverter.slx`) for studying a three-phase inverter operating with 180-degree conduction.

In 180-degree conduction mode, each power switch is commanded to conduct for 180 electrical degrees per cycle. The six switches are controlled with gate signals shifted in sequence, allowing a three-phase AC output to be synthesized from a DC source.

## Project File
- `Three_phase_180_degree_inverter.slx` — MATLAB/Simulink model of the inverter.

## Requirements
- MATLAB
- Simulink
- Any additional Simulink toolboxes required by the blocks used in the model

The required MATLAB release and toolboxes depend on the components used in the model.

## How to Run
1. Open MATLAB with Simulink installed.
2. Set the MATLAB Current Folder to the directory containing `Three_phase_180_degree_inverter.slx`.
3. Open the model in Simulink.
4. Review the DC source, inverter bridge, gate-pulse generation, load, and measurement blocks.
5. Check the simulation stop time and solver settings.
6. Click **Run** to simulate the model.
7. Use the available scopes or logged signals to inspect gate pulses, phase voltages, line-to-line voltages, and phase currents.

You can also open the model from the MATLAB Command Window:

```matlab
open_system('Three_phase_180_degree_inverter.slx');
```

## Operating Principle
A conventional three-phase bridge inverter uses six controlled power switches. In 180-degree conduction mode, each switch receives a gate command spanning 180 electrical degrees. The six switching commands are typically displaced by 60 electrical degrees from one another. Depending on the switching state, three switches may conduct at a time—often one switch in each phase leg—subject to the bridge's switching sequence and device arrangement.

The inverter converts DC input power into a stepped three-phase AC output. The actual voltage and current waveforms depend on the DC-link voltage, switching sequence, load connection, and load parameters.

## Suggested Checks
- Confirm that all six gate signals follow the intended 180-degree conduction pattern.
- Verify the 60-degree displacement between successive switching commands.
- Check that upper and lower switches in each inverter leg are not commanded on simultaneously.
- Verify DC-link voltage, load connection, and load parameters.
- Inspect phase and line-to-line voltage waveforms.
- Inspect phase currents and compare them with the expected response of the selected load.
- Review simulation warnings, current spikes, and solver settings.

## Expected Observations
A conventional three-phase 180-degree conduction inverter generally produces stepped phase and line-to-line voltage waveforms. With a balanced load, the three phase waveforms should be displaced by approximately 120 electrical degrees. Current waveforms depend on the load type and its electrical parameters.

Use the actual simulation outputs to document numerical results; no performance values are assumed in this README.

## Notes
- This README describes the standard principle of a three-phase 180-degree conduction inverter. Confirm the specific topology, switching logic, parameters, and outputs by inspecting the supplied Simulink model.
- For an academic submission, consider adding the circuit diagram, parameter table, scope screenshots, and a short discussion of the simulated results.

## License
This Project is Under MIT license.
