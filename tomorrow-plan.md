# Tomorrow's Detailed Content

Date planned: 2026-06-29
Study duration: 2 hours by default
Topic: Buck converter basics, with hardware/software/analog support perspective
Current gate: Buck principle gate, with analog entry support
Study mode: The learner finds learning resources independently, asks Codex when stuck, then submits notes/artifacts for assessment.
Frontier note: No GaN/SiC assessment tomorrow. After the classic Buck foundation is acceptable, Codex will add a silicon MOSFET Buck versus GaN Buck comparison.

## Learning Objectives

By the end of the session, the learner should be able to:

1. Explain what a Buck converter does.
2. Draw or describe the current path when the MOS is on.
3. Draw or describe the current path when the MOS is off.
4. Use the ideal CCM formula `Vout = D * Vin`.
5. Identify the main Buck hardware blocks.
6. Explain why a controller needs analog front-end circuits such as a resistor divider and RC filter before ADC sampling.
7. Name the basic instruments that would be used later to observe Buck behavior: DC supply, oscilloscope, probe, electronic load or load resistor, multimeter.

## Pre-Study Review

Review these ideas first:

1. Voltage is electrical potential difference.
2. Current is charge flow.
3. A capacitor voltage cannot change instantly.
4. An inductor current cannot change instantly.
5. A switch-mode power supply controls energy transfer by switching quickly.
6. Safety idea: even for low-voltage work, power-up should be current-limited and changes should be made one at a time.

## New Knowledge

Study these points:

1. Buck is a step-down DC/DC converter.
2. MOS on-state:
   - Input supplies energy to the inductor, capacitor, and load.
   - Inductor current rises.
3. MOS off-state:
   - Inductor keeps current flowing through diode or synchronous MOS path.
   - Inductor current falls.
4. Ideal continuous conduction mode relationship:
   - `Vout = D * Vin`
   - `D = Vout / Vin`
5. Key waveforms:
   - PWM gate signal.
   - Switch node voltage.
   - Inductor current ripple.
   - Output voltage ripple.
6. Main hardware blocks:
   - MOSFET or switching device.
   - Diode or synchronous MOS.
   - Inductor.
   - Output capacitor.
   - Gate driver.
   - Voltage/current sensing.
   - Protection circuit.
7. Analog support:
   - The MCU ADC cannot directly sample high output voltage.
   - A resistor divider scales voltage down.
   - An RC filter reduces switching noise before ADC sampling.
8. Engineering observation:
   - Later, a real Buck is verified by measuring gate signal, switch node, inductor current, output voltage, and output ripple.
   - Tomorrow only requires knowing these names, not using instruments yet.

## Hands-On Tasks

1. Draw a Buck topology.
2. Mark the MOS on-state current path.
3. Mark the MOS off-state current path.
4. Sketch PWM, switch node voltage, inductor current, and output voltage ripple.
5. Draw a simple output-voltage sensing path: `Vout -> resistor divider -> RC filter -> ADC`.
6. Solve the three duty-cycle exercises.
7. Make a short table with two columns: "Buck part" and "what it does".

## Exercises

1. `Vin = 24V`, target `Vout = 12V`: calculate duty cycle.
2. `Vin = 48V`, target `Vout = 12V`: calculate duty cycle.
3. `Vin = 60V`, `D = 0.2`: calculate ideal output voltage.

## Submit Back To Codex

After studying, send:

1. Buck function.
2. Current path when MOS is on.
3. Current path when MOS is off.
4. Duty-cycle formula and three exercise answers.
5. Main hardware blocks.
6. Why Buck voltage sensing needs a resistor divider and RC filter.
7. Basic instrument names for observing a Buck later.
8. Sketch/photo/simulation/code if available.
9. Questions you still have.

## Assessment Questions

Codex will ask or check these:

1. Why does Buck output voltage decrease when duty cycle decreases?
2. When the MOS turns off, why does the load current not immediately become zero?
3. In ideal CCM, if `Vin = 36V` and `D = 0.25`, what is `Vout`?
4. Why can an MCU ADC usually not measure Buck output voltage directly?
5. What problem does an RC filter before ADC help reduce?
6. If a Buck output target is 5V from 20V input, what ideal duty cycle is needed?
7. Which waveform would you expect at the switch node: DC, sine wave, or pulse waveform? Why?

## Passing Criteria

The Buck principle gate can move from `Not started` toward `Learning` or `Working depth` only if evidence shows:

1. Current paths are mostly correct.
2. Duty-cycle calculations are correct.
3. Key waveforms are qualitatively correct.
4. Main hardware blocks are identified.
5. The analog sensing explanation is basically correct.
6. The learner can identify at least three basic instruments or measurement targets for future Buck debugging.

The learner does not self-certify passing. Codex reviews evidence, asks follow-up questions if needed, then assigns the current level.

## Codex Will Check

1. Whether the current paths are physically valid.
2. Whether the duty-cycle formula is applied correctly.
3. Whether waveform sketches match Buck behavior.
4. Whether hardware blocks are complete enough for this stage.
5. Whether the resistor divider and RC filter explanation shows basic analog understanding.
6. Whether the learner knows this is only the first Buck principle/analog-entry assessment, not full Buck mastery.
