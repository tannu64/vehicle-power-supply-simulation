# Power Supply Circuit Simulation

## Project Overview
This project involves the analysis of a motor vehicle power supply circuit using MultiSim software. The simulation includes a transformer, diodes, and resistors to investigate their properties and the effects of varying component parameters.

## Circuit Description
The simulation is based on a power supply circuit that converts AC to DC. The circuit includes:
- A transformer with adjustable turns ratio
- A bridge rectifier using diodes
- A filter capacitor (C1)
- A load resistor (R1)

## Key Investigations

### 1. Basic Operation
The oscilloscope was used to monitor:
- AC input voltage across the secondary windings of the transformer (Channel 1)
- DC output voltage across the load resistor R1 (Channel 2)

The scaling functions on the oscilloscope were adjusted to display 3-4 cycles of the waveform for clear visualization.

### 2. Capacitance Variation Effects
The capacitor C1 was varied from 10μF to 100μF in steps of 10μF. Key observations:
- As capacitance increases, the ripple factor in the rectified output decreases
- Higher capacitance values provide smoother DC output by improving the filtering of AC components
- The charging and discharging time of the capacitor affects the shape of the output waveform

#### Detailed Analysis of Ripple Reduction
When analyzing the oscilloscope readings across the tested capacitance values (10μF to 100μF):

- **At 10μF**: The ripple voltage was at its maximum, showing significant voltage fluctuations in the output waveform
- **At 50μF**: The ripple voltage was noticeably reduced compared to the 10μF configuration
- **At 100μF**: The ripple voltage reached its minimum among the tested values, providing the smoothest DC output

This behavior can be explained by the relationship between capacitance and ripple voltage:

```
Vr = I / (f × C)
```

Where:
- Vr is the ripple voltage
- I is the load current
- f is the frequency of the input voltage
- C is the capacitance

From this equation, it's clear that increasing the capacitance (C) results in a proportional decrease in ripple voltage (Vr), which is exactly what we observed in the simulation.

### 3. Transformer Turns Ratio Effects
The transformer turns ratio was changed from 10:1 to 100:1 with C1 set to 100μF. This resulted in:
- A change in the output voltage across R1
- The higher turns ratio (100:1) produced a lower output voltage due to the inverse relationship between turns ratio and secondary voltage

## Files in the Repository
- `Design1.ms14` - Initial circuit design in MultiSim
- `Design2.ms14` - Modified circuit design with different component parameters
- `Task 8_report.pdf` - Detailed report of the simulation and findings
- `Task 8.docx` - Written documentation of the task
- `Task8.mp4` - Video demonstration of the simulation

## Project Documentation

### Detailed Report PDF
You can view the detailed report by:
1. Clicking on the `Task 8_report.pdf` file in the repository
2. Using this direct link to view the PDF: [Task 8 Report](Task%208_report.pdf)
3. Or view it through GitHub's PDF viewer with this link: <a href="https://docs.github.com/viewscreen/pdf?url=https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/Task%208_report.pdf">View PDF Report</a> (Remember to update YOUR_USERNAME and YOUR_REPO_NAME with your actual GitHub username and repository name)

### Waveform Screenshots
To properly display the waveform screenshots in this README:
1. Create a `screenshots` directory in your repository
2. Extract images from the PDF or simulation and save them to this directory
3. Name one of the key oscilloscope images `oscilloscope_output.png`

Example screenshot reference:
![Oscilloscope Output](/screenshots/oscilloscope_output.png)
*Figure: AC input (yellow) and DC output with ripple (blue)*

## How to Run the Simulation
1. Open the .ms14 files using MultiSim software
2. The circuits are pre-configured with the necessary components and measurement tools
3. Run the simulation to observe the effects of different component values
4. Use the oscilloscope to monitor input and output waveforms

## Observations and Conclusions
- The filter capacitor plays a crucial role in reducing ripple in the DC output
- Increasing the capacitance value results in smoother DC output
- The transformer turns ratio directly affects the output voltage level
- This simulation provides a safe way to investigate power supply characteristics without the hazards of damaging an actual vehicle's system 