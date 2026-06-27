# 24-Month Power Electronics Full-Stack Roadmap

## Overview

This roadmap assumes usually about 2 hours of study per day, with flexible progress on holidays or busy days. The upgraded goal is not only digital power software. The goal is to master major power topologies from both hardware and software perspectives.

The learner already has STM32, PC tool, CPLD, control-board, and communication experience. The plan therefore focuses on:

- Power topology principles.
- Hardware design and component selection.
- Magnetic components and power-stage behavior.
- Digital control software.
- Simulation.
- Real hardware bring-up and debugging.
- Product-level architecture and documentation.

## Topology Mastery Gates

For each major topology, learning is tracked through five gates:

| Gate | Meaning |
|---|---|
| Principle | Draw topology, current paths, switching states, key waveforms, operating modes |
| Hardware | Choose or calculate switches, magnetics, capacitors, drivers, sensing, protection, thermal, layout |
| Simulation | Build open-loop and closed-loop simulation when applicable; explain normal and abnormal waveforms |
| Software/control | PWM strategy, ADC sampling, loop control, soft start, protection, state machine |
| Debug | Measurement points, oscilloscope interpretation, safe bring-up, common faults |

A topology can move forward after engineering working depth. Product-level mastery is revisited later through projects and debug cases.

## Milestone Summary

| Period | Main Goal | Expected Capability |
|---|---|---|
| Month 1 | Buck foundation | Understand Buck principle, hardware blocks, key waveforms, basic sizing |
| Month 2 | Buck control and debug foundation | PWM/ADC/PI/soft start/protection around Buck |
| Month 3 | Boost and Buck-Boost | Compare energy paths, stress, control differences |
| Month 4 | Non-isolated DC/DC design practice | Simulate and size Buck/Boost/Buck-Boost; start hardware design notes |
| Months 5-6 | TI C2000/DSP and digital control platform | Build reusable PWM/ADC/control/protection software base |
| Months 7-8 | Real low-voltage Buck/Boost project | Bring up, measure, close loop, debug safely |
| Months 9-10 | Isolated DC/DC foundation | Flyback, forward, push-pull, half bridge, full bridge |
| Months 11-12 | Resonant and bridge topologies | LLC and phase-shift full bridge at principle/hardware/control level |
| Months 13-14 | AC/DC and PFC | Rectifier, single-phase PFC, Boost PFC control, protection |
| Months 15-16 | DC/AC inverter | Half/full bridge inverter, SPWM/SVPWM basics, sampling, protection |
| Months 17-18 | Bidirectional and vehicle power overview | Bidirectional Buck-Boost, vehicle DC/DC, OBC system view |
| Months 19-20 | Hardware depth | Magnetics, losses, thermal, layout, sensing, protection coordination |
| Months 21-22 | Software architecture depth | Platform drivers, fault manager, calibration, CAN, logging, parameter management |
| Months 23-24 | Integrated portfolio and interview readiness | Document topology library, projects, debug cases, design reviews |

## Phase 1: Months 1-2 - Buck As The Master Template

Focus:

- Buck topology and switching states.
- CCM/DCM.
- Inductor ripple and capacitor ripple.
- MOSFET, diode/synchronous MOS, driver, bootstrap basics.
- Voltage/current sensing.
- Layout priorities: hot loop, power ground, signal ground, sampling path.
- PWM, dead time, ADC synchronization.
- PI voltage loop, current limit, soft start, OVP/UVP/OCP/SCP.
- Open-loop and closed-loop Buck simulation.

Outputs:

- Buck principle notes.
- Buck hardware block diagram.
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
- Control strategy comparison notes.

## Phase 3: Months 5-6 - Digital Control Platform

Focus:

- TI C2000 and STM32 comparison for digital power.
- ePWM/complementary PWM/dead-band.
- ADC triggered by PWM.
- Control-loop ISR.
- CMPSS and Trip Zone.
- CLA/HRPWM awareness.
- Fixed-point/float control considerations.
- CAN/SCI telemetry.

Outputs:

- C2000 or STM32 PWM/ADC synchronized demo.
- PI loop code skeleton.
- Trip/protection demo.
- Telemetry demo.
- Reusable digital power software framework draft.

## Phase 4: Months 7-8 - Real Low-Voltage DC/DC Project

Focus:

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

Outputs:

- Bidirectional converter mode table.
- Vehicle power system block diagram.
- CAN signal draft.
- System fault-state diagram.

## Phase 10: Months 19-20 - Hardware Depth

Focus:

- Magnetics: inductors, transformers, saturation, core loss, copper loss.
- Semiconductor loss: conduction loss, switching loss, diode recovery.
- Gate drive and dead time.
- Snubber and clamp concepts.
- Current sensing: shunt, Hall, CT, amplifier, layout.
- Thermal path and derating.
- PCB layout for power converters.
- EMI/EMC awareness.

Outputs:

- Hardware design checklist.
- Loss calculation examples.
- Layout review checklist.
- Debug case notes.

## Phase 11: Months 21-22 - Software Architecture Depth

Focus:

- Platform drivers.
- Control-loop abstraction.
- Fault manager.
- Protection priority and latching/recovery.
- Parameter management.
- Calibration.
- CAN/CANopen/J1939/UDS awareness depending on target role.
- Logging and diagnostic codes.
- Bootloader/upgrade awareness.

Outputs:

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
