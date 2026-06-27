# 24-Month Power Electronics Full-Stack Roadmap

## Overview

This roadmap assumes usually about 2 hours of study per day, with flexible progress on holidays or busy days. The upgraded goal is not only digital power software. The goal is to master major power topologies from both hardware and software perspectives.

The learner already has STM32, PC tool, CPLD, control-board, and communication experience. The plan therefore focuses on:

- Power topology principles.
- Analog electronics foundation.
- Hardware design and component selection.
- Magnetic components and power-stage behavior.
- Digital control software.
- Simulation.
- Real hardware bring-up and debugging.
- Product-level architecture and documentation.
- Engineering workflow: datasheets, requirements, BOM, derating, reliability, safety, test plans, design reviews.
- Industry frontier awareness: GaN, SiC, high-frequency conversion, advanced packaging, planar magnetics, totem-pole PFC, bidirectional converters, vehicle/data-center power trends.

## Topology Mastery Gates

For each major topology, learning is tracked through these gates:

| Gate | Meaning |
|---|---|
| Principle | Draw topology, current paths, switching states, key waveforms, operating modes |
| Hardware | Choose or calculate switches, magnetics, capacitors, drivers, sensing, protection, thermal, layout |
| Analog support | Understand sensing, filtering, op-amps, comparators, references, compensation, noise, grounding |
| Simulation | Build open-loop and closed-loop simulation when applicable; explain normal and abnormal waveforms |
| Software/control | PWM strategy, ADC sampling, loop control, soft start, protection, state machine |
| Debug | Measurement points, oscilloscope interpretation, safe bring-up, common faults |
| Frontier awareness | Compare classic implementation with modern industry approaches such as GaN/SiC/high-frequency designs |

A topology can move forward after engineering working depth. Product-level mastery is revisited later through projects and debug cases.

## Milestone Summary

| Period | Main Goal | Expected Capability |
|---|---|---|
| Month 1 | Buck + analog entry foundation | Understand Buck principle plus resistor/capacitor/diode/RC basics |
| Month 2 | Buck control, sensing, and protection foundation | PWM/ADC/PI plus voltage/current sensing, filters, comparators |
| Month 3 | Boost and Buck-Boost | Compare energy paths, stress, control differences |
| Month 4 | Non-isolated DC/DC and analog front ends | Simulate and size Buck/Boost/Buck-Boost; design sampling/filter notes |
| Months 5-6 | TI C2000/DSP and analog-aware digital control platform | Build reusable PWM/ADC/control/protection base with analog assumptions |
| Months 7-8 | Real low-voltage Buck/Boost project | Bring up, measure, close loop, debug safely |
| Months 9-10 | Isolated DC/DC foundation | Flyback, forward, push-pull, half bridge, full bridge |
| Months 11-12 | Resonant and bridge topologies | LLC and phase-shift full bridge at principle/hardware/control level |
| Months 13-14 | AC/DC and PFC | Rectifier, single-phase PFC, Boost PFC control, protection |
| Months 15-16 | DC/AC inverter | Half/full bridge inverter, SPWM/SVPWM basics, sampling, protection |
| Months 17-18 | Bidirectional and vehicle power overview | Bidirectional Buck-Boost, vehicle DC/DC, OBC system view |
| Months 19-20 | Hardware depth | Magnetics, losses, thermal, layout, sensing, protection coordination |
| Months 21-22 | Product engineering depth | Software architecture plus requirements, test plans, datasheets, BOM, derating, safety |
| Months 23-24 | Integrated portfolio and interview readiness | Document topology library, projects, debug cases, design reviews |

## Phase 1: Months 1-2 - Buck As The Master Template

Focus:

- Analog entry: voltage, current, resistor divider, capacitor charging, RC time constant, diode behavior.
- Buck topology and switching states.
- CCM/DCM.
- Inductor ripple and capacitor ripple.
- MOSFET, diode/synchronous MOS, driver, bootstrap basics.
- Voltage/current sensing.
- RC filter before ADC.
- Op-amp and comparator awareness for sensing/protection.
- Layout priorities: hot loop, power ground, signal ground, sampling path.
- PWM, dead time, ADC synchronization.
- PI voltage loop, current limit, soft start, OVP/UVP/OCP/SCP.
- Open-loop and closed-loop Buck simulation.
- Frontier preview after foundation: silicon MOSFET Buck versus high-frequency GaN Buck.

Outputs:

- Buck principle notes.
- Buck hardware block diagram.
- Analog support notes for Buck voltage sensing and current sensing.
- Basic sizing spreadsheet or notes.
- Buck open-loop simulation.
- Buck voltage-loop pseudocode.
- Safe bring-up checklist.

## Phase 2: Months 3-4 - Non-Isolated DC/DC Family

Topologies:

- Boost.
- Buck-Boost.
- Inverting Buck-Boost.
- Synchronous Buck/Boost.
- Intro to bidirectional Buck-Boost.

Focus:

- Analog support for non-isolated DC/DC: voltage dividers, current-sense resistor, RC anti-alias filters, op-amp gain, comparator thresholds.
- Energy storage and transfer paths.
- Switch and diode/MOS voltage/current stress.
- Duty-cycle relationships and limits.
- Inductor and capacitor sizing.
- Current sensing positions.
- Control differences between Buck and Boost.
- Load-step and input-step behavior.

Outputs:

- Topology comparison table.
- Boost and Buck-Boost simulations.
- Hardware sizing examples.
- Sampling and protection front-end examples.
- Control strategy comparison notes.
- Classic versus GaN/SiC non-isolated DC/DC comparison.

## Phase 3: Months 5-6 - Digital Control Platform

Focus:

- TI C2000 and STM32 comparison for digital power.
- ePWM/complementary PWM/dead-band.
- ADC triggered by PWM.
- ADC input constraints, source impedance, sampling capacitor awareness, RC filter tradeoffs.
- Control-loop ISR.
- CMPSS and Trip Zone.
- Analog comparator versus MCU ADC protection path.
- CLA/HRPWM awareness.
- Fixed-point/float control considerations.
- CAN/SCI telemetry.
- Digital control trends: faster control loops, model-based design, auto-code generation awareness.

Outputs:

- C2000 or STM32 PWM/ADC synchronized demo.
- PI loop code skeleton.
- Trip/protection demo.
- Telemetry demo.
- Reusable digital power software framework draft.

## Phase 4: Months 7-8 - Real Low-Voltage DC/DC Project

Focus:

- Safety setup: current limit, fusing awareness, discharge path, isolated measurement awareness, one-change-at-a-time debug discipline.
- Safe low-voltage Buck and, if possible, Boost hardware.
- Current-limited power-up.
- Open-loop validation.
- ADC scaling and calibration.
- Closed-loop voltage regulation.
- Soft start and protection.
- Oscilloscope measurement of switch node, gate, inductor current, output ripple.

Outputs:

- Working Buck closed-loop demo.
- Optional Boost demo.
- Debug notes and waveform screenshots.
- Fault table.
- Test plan and test report.
- Short project report.

## Phase 5: Months 9-10 - Isolated DC/DC Foundation

Topologies:

- Flyback.
- Forward.
- Push-pull.
- Half bridge.
- Full bridge.

Focus:

- Transformer action and isolation.
- Magnetizing current.
- Reset paths and demagnetization.
- Leakage inductance and spikes.
- Snubber/clamp basics.
- Primary/secondary device stress.
- Optocoupler/TL431 feedback awareness.
- Digital control options for isolated converters.

Outputs:

- Isolated topology comparison table.
- Flyback and forward current-path notes.
- Basic transformer/magnetics notes.
- Simulation of at least one isolated topology.

## Phase 6: Months 11-12 - LLC And Phase-Shift Full Bridge

Topologies:

- LLC resonant converter.
- Phase-shift full bridge.

Focus:

- Resonant tank basics: Lr, Cr, Lm.
- Frequency control.
- ZVS/ZCS intuition.
- Synchronous rectification awareness.
- Phase-shift control and duty/effective duty.
- Light-load behavior and protection.
- Practical debugging waveforms.
- Frontier comparison: high-frequency LLC/PSFB, GaN/SiC switches, planar magnetics.

Outputs:

- LLC operating-region notes.
- PSFB switching-state notes.
- Simulation screenshots.
- Control and protection comparison notes.

## Phase 7: Months 13-14 - AC/DC And PFC

Topologies:

- Diode rectifier.
- Single-phase Boost PFC.
- Totem-pole PFC awareness.

Focus:

- Rectified mains waveform.
- Power factor and harmonic current.
- Boost PFC power stage.
- Voltage loop and current loop.
- Feedforward and input-voltage sampling.
- Inrush, bus OVP, brown-in/brown-out, current protection.
- Safety and isolation awareness.
- Frontier comparison: bridge Boost PFC versus totem-pole PFC using GaN/SiC.

Outputs:

- PFC block diagram.
- PFC current-loop explanation.
- Simulation or detailed waveform analysis.
- Protection checklist.

## Phase 8: Months 15-16 - DC/AC Inverter

Topologies:

- Half-bridge inverter.
- Full-bridge inverter.
- Three-phase inverter overview.

Focus:

- SPWM.
- SVPWM basics.
- Dead time and shoot-through prevention.
- Bus voltage sampling.
- Phase current sampling.
- Overcurrent/desaturation protection awareness.
- Output filter basics.
- Frontier comparison: silicon/IGBT inverter versus SiC inverter.

Outputs:

- Inverter switching-state notes.
- SPWM waveform notes.
- Protection and sampling notes.
- Simulation or software PWM demo.

## Phase 9: Months 17-18 - Bidirectional And Vehicle Power Systems

Topologies/systems:

- Bidirectional Buck-Boost.
- Vehicle low-voltage DC/DC.
- OBC system overview.
- Battery interface basics.

Focus:

- Power direction control.
- Charge/discharge modes.
- Precharge and contactor awareness.
- CAN communication and diagnostics.
- Fault recovery and derating.
- System-level state machine.
- Frontier comparison: CLLC, bidirectional OBC, 800V vehicle platforms, energy storage converters.

Outputs:

- Bidirectional converter mode table.
- Vehicle power system block diagram.
- CAN signal draft.
- System fault-state diagram.

## Phase 10: Months 19-20 - Hardware Depth

Focus:

- Analog electronics consolidation: op-amp limitations, comparator hysteresis, references, biasing, noise, bandwidth, phase shift.
- Magnetics: inductors, transformers, saturation, core loss, copper loss.
- Semiconductor loss: conduction loss, switching loss, diode recovery.
- Gate drive and dead time.
- Snubber and clamp concepts.
- Current sensing: shunt, Hall, CT, amplifier, layout.
- Thermal path and derating.
- PCB layout for power converters.
- EMI/EMC awareness.
- Wide-bandgap layout and EMI challenges.
- Datasheet reading and parameter extraction.
- BOM awareness and second-source thinking.
- Derating and reliability basics.

Outputs:

- Hardware design checklist.
- Loss calculation examples.
- Layout review checklist.
- Datasheet parameter checklist.
- Debug case notes.

## Phase 11: Months 21-22 - Product Engineering And Software Architecture Depth

Focus:

- Requirement decomposition: input/output range, load, ripple, transient, protection, thermal, communication, safety.
- Test plan design: startup, load step, input step, protection, thermal, communication, fault recovery.
- Design-review writing: assumptions, risks, calculations, waveforms, verification evidence.
- Platform drivers.
- Control-loop abstraction.
- Fault manager.
- Protection priority and latching/recovery.
- Parameter management.
- Calibration.
- CAN/CANopen/J1939/UDS awareness depending on target role.
- Logging and diagnostic codes.
- Bootloader/upgrade awareness.
- Version control and release notes for learning projects.

Outputs:

- Requirement table.
- Test plan and test report template.
- Design-review document.
- Product-like digital power software framework.
- Fault table.
- Parameter table.
- Communication protocol draft.
- Architecture diagram.

## Phase 12: Months 23-24 - Portfolio And Expert Review

Focus:

- Build a topology library.
- Organize all notes by topology and mastery gate.
- Finish at least one strong real or simulated project report.
- Practice design reviews.
- Prepare interview explanations.
- Identify remaining gaps for the next 12-24 months.

Outputs:

- Topology mastery matrix.
- Portfolio project document.
- Interview Q&A bank.
- Final gap review.

## Long-Term After 24 Months

The 24-month plan is enough to build a strong full-stack foundation. True mastery continues through:

- More real hardware projects.
- Higher power levels.
- Product failures and debug cases.
- EMI/thermal/compliance work.
- Reading reference designs and application notes.
- Repeated design reviews.
- Safety and compliance standards awareness.
- Supplier component changes and reliability cases.
- Frontier-technology roadmap reviews.
