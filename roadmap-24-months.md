# 24-Month Digital Power Learning Roadmap

## Overview

This roadmap assumes about 2 hours of study per day. The learner already has STM32, PC tool, CPLD, control-board, and communication experience. The plan focuses on power electronics, digital control, C2000/DSP, simulation, and product-level power software.

## Milestone Summary

| Period | Main Goal | Expected Capability |
|---|---|---|
| Month 1 | Power electronics foundation | Explain Buck/Boost and basic current paths/waveforms |
| Month 2 | Digital control foundation | Explain PWM/ADC timing, PI control, soft start, protection |
| Months 3-4 | Simulation | Build Buck/Boost open-loop and closed-loop simulations |
| Months 5-6 | TI C2000/DSP | Implement PWM, ADC sampling, interrupt loop, PI, protection |
| Months 7-8 | Real Buck project | Tune a real or development-board Buck closed loop safely |
| Months 9-10 | Product software architecture | Build state machine, fault handling, parameters, CAN telemetry |
| Months 11-12 | Intermediate topologies | Understand PFC, inverter, LLC, full bridge, vehicle power structure |
| Months 13-18 | Project depth | Build stronger demos, improve loop tuning, debugging, documentation |
| Months 19-24 | Senior-level preparation | Platformization, design review thinking, interview/project packaging |

## Phase 1: Month 1 - Power Electronics Foundation

Focus:

- Buck converter.
- Boost converter.
- Buck-Boost converter.
- Diode vs synchronous rectification.
- Inductor and capacitor roles.
- Continuous conduction mode and discontinuous conduction mode.
- MOSFET switching, dead time, freewheeling path.
- Basic rectifier/inverter/PFC/LLC awareness.

Outputs:

- Hand-drawn topology notes.
- Current-path diagrams.
- Key waveform sketches.
- Simple duty-cycle calculations.

## Phase 2: Month 2 - Digital Control Foundation

Focus:

- PWM frequency, duty cycle, dead time.
- ADC sampling timing and PWM synchronization.
- Discrete PI/PID basics.
- Voltage loop and current loop.
- Soft start.
- Protection logic: OVP, UVP, OCP, SCP, OTP.
- Power state machine.

Outputs:

- Pseudocode for Buck voltage-loop control.
- A basic power state machine diagram.
- A protection list with trigger, action, and recovery behavior.

## Phase 3: Months 3-4 - Simulation

Preferred tools:

- Start with PSIM or PLECS for power electronics.
- Use MATLAB/Simulink for control concepts when needed.

Focus:

- Buck open-loop simulation.
- Buck closed-loop simulation with PI.
- Load-step response.
- Input-voltage change response.
- Boost open-loop and closed-loop simulation.
- Fault/protection simulation.

Outputs:

- Simulation files.
- Screenshots of waveforms.
- Notes explaining response, overshoot, settling, and instability.

## Phase 4: Months 5-6 - TI C2000/DSP

Focus:

- Code Composer Studio.
- TI C2000 project structure.
- ePWM and complementary PWM.
- Dead-band module.
- ADC triggered by PWM.
- Control-loop ISR.
- CMPSS and Trip Zone.
- CLA basics.
- HRPWM awareness.
- CAN/SCI telemetry.

Recommended hardware:

- TI C2000 LaunchPad such as F280049C, F280039C, or F28379D.

Outputs:

- PWM demo.
- ADC synchronized sampling demo.
- ISR PI loop demo.
- Trip Zone protection demo.
- Simple telemetry demo.

## Phase 5: Months 7-8 - Real Buck Project

Focus:

- Safe low-voltage Buck hardware or development kit.
- Open-loop bring-up.
- ADC scaling and calibration.
- Closed-loop voltage regulation.
- Soft start.
- Current limit and voltage protection.
- Oscilloscope waveform analysis.

Outputs:

- Working Buck closed-loop demo.
- Debug notes.
- Safety checklist.
- Short project report.

## Phase 6: Months 9-10 - Product Software Architecture

Focus:

- Power state machine.
- Fault management.
- Protection priority.
- Parameter storage.
- Calibration.
- CAN communication.
- Upper-computer telemetry.
- Logging and diagnostic codes.
- Bootloader/upgrade awareness.

Outputs:

- Product-like digital power software framework.
- CAN telemetry protocol.
- Fault table.
- State-machine diagram.

## Phase 7: Months 11-12 - Intermediate Topologies

Focus:

- PFC basics.
- LLC basics.
- Full bridge and phase shift full bridge.
- Inverter basics.
- Vehicle OBC and DC/DC overview.
- Multi-loop and multi-mode control awareness.

Outputs:

- Topology comparison notes.
- Interview-oriented explanation sheets.
- JD keyword map.

## Phase 8: Months 13-18 - Project Depth

Focus:

- Improve Buck/Boost project quality.
- Add robust communication and monitoring.
- Try one higher-level topology simulation.
- Improve PI tuning intuition.
- Practice hardware debugging scenarios.
- Read application notes and reference designs.

Outputs:

- Strong portfolio project.
- Debug case library.
- Simulation report.
- Resume project bullet drafts.

## Phase 9: Months 19-24 - Senior-Level Preparation

Focus:

- Platformization and reusable drivers.
- Software architecture review.
- Design documents.
- Technical risk analysis.
- Customer requirement translation.
- Interview practice.
- Advanced topics: EMI awareness, sampling noise, loop stability, protection coordination.

Outputs:

- Senior-style project documentation.
- Architecture diagrams.
- Interview Q&A bank.
- Final skill-gap review.
