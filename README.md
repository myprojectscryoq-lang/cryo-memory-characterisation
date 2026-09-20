# cryo-memory-characterisation
LTspice characterisation of 6T SRAM and 4T DRAM cells from -196°C to 100°C: static noise margin, Vth shift, write margin, and noise floor analysis.
Cryogenic-to-Hot Characterisation of 6T SRAM and 4T DRAM Cells (LTspice)

SPICE-based characterisation of 6T SRAM and 4T DRAM memory cells across a wide temperature range (-196 °C to 100 °C) using LTspice. The project looks at how temperature affects cell stability, threshold voltage, write capability, and readout noise, with a focus on identifying the main reliability bottleneck at low temperatures.

This repository is a results showcase. It contains labelled simulation screenshots and a summary of findings. Design files are not included.

Key Results
Characterised 6T SRAM and DRAM cells across a temperature sweep from -196 °C to 100 °C using LTspice. Extracted static noise margins (SNM), threshold voltage shifts, and write margin degradation, identifying write margin as the primary reliability bottleneck at low temperatures.
Extracted the noise floor of a 4T DRAM topology: flat output noise of ~4.7 nV/√Hz, corner frequency of ~1 MHz, and SNR ≫ 110.9 dB, demonstrating noise-limited readout characterisation relevant to analog/mixed-signal design.
Tools and Setup
Item	Details
Simulator	LTspice
Circuits	6T SRAM cell, 4T DRAM cell
Temperature sweep	-196 °C to 100 °C (sweep range is visible in each schematic)
Supply voltage (VDD)	[0.7v]
Transistor models	[NMOS PMOS]
Analyses	DC sweep (SNM), transient (write margin), .noise (noise floor)


Observations
Write margin degrades as temperature drops, making writes the limiting factor for reliable operation at low temperature.
Threshold voltage shifts with temperature, which feeds into the changes in SNM and write margin.
Readout noise of the 4T DRAM is flat at ~4.7 nV/√Hz with a corner frequency near 1 MHz, so readout is noise-limited rather than signal-limited at the operating point simulated.



Limitations

Standard SPICE MOSFET models are generally not validated at cryogenic temperatures and may not capture effects such as carrier freeze-out. Results at -196 °C should be read as model-based trends, not silicon-accurate values. The noise results depend on the noise models included in the simulation.



License

Released under the MIT License.
