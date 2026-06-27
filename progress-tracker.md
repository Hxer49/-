# Progress Tracker

## Current Phase

- Phase: Months 1-2 - Buck as the master template.
- Current topic: Buck converter basics.
- Status: Not started.
- Planning mode: Dynamic. Advance, review, expand, or slow down based on actual daily notes.
- Upgraded target: topology full-stack mastery, including hardware and software.

## Completed Topics

| Date | Topic | Evidence |
|---|---|---|
| 2026-06-28 | Long-term learning system setup | Learning archive created |
| 2026-06-28 | Goal upgrade | Target changed to full-stack power topology mastery |

## Topology Mastery Matrix

Status values:

- Not started
- Learning
- Working depth
- Project depth
- Review later

| Topology/System | Principle | Hardware | Simulation | Software/control | Debug | Notes |
|---|---|---|---|---|---|---|
| Buck | Not started | Not started | Not started | Not started | Not started | First master template |
| Boost | Not started | Not started | Not started | Not started | Not started | Planned after Buck foundation |
| Buck-Boost | Not started | Not started | Not started | Not started | Not started | Non-isolated family |
| Synchronous Buck/Boost | Not started | Not started | Not started | Not started | Not started | Dead time and driver focus |
| Bidirectional Buck-Boost | Not started | Not started | Not started | Not started | Not started | Later vehicle/system topic |
| Flyback | Not started | Not started | Not started | Not started | Not started | Isolated foundation |
| Forward | Not started | Not started | Not started | Not started | Not started | Isolated foundation |
| Push-pull | Not started | Not started | Not started | Not started | Not started | Isolated foundation |
| Half bridge DC/DC | Not started | Not started | Not started | Not started | Not started | Bridge family |
| Full bridge DC/DC | Not started | Not started | Not started | Not started | Not started | Bridge family |
| Phase-shift full bridge | Not started | Not started | Not started | Not started | Not started | Advanced bridge |
| LLC | Not started | Not started | Not started | Not started | Not started | Resonant converter |
| Rectifier AC/DC | Not started | Not started | Not started | Not started | Not started | AC/DC foundation |
| Boost PFC | Not started | Not started | Not started | Not started | Not started | AC/DC control focus |
| Totem-pole PFC | Not started | Not started | Not started | Not started | Not started | Awareness first |
| Half-bridge inverter | Not started | Not started | Not started | Not started | Not started | DC/AC foundation |
| Full-bridge inverter | Not started | Not started | Not started | Not started | Not started | DC/AC foundation |
| Three-phase inverter | Not started | Not started | Not started | Not started | Not started | Overview first |
| Vehicle DC/DC | Not started | Not started | Not started | Not started | Not started | System integration |
| OBC system | Not started | Not started | Not started | Not started | Not started | System integration |

## Cross-Cutting Skill Checklist

| Skill Area | Status | Notes |
|---|---|---|
| Power topology current paths | Not started | Start with Buck |
| Magnetics: inductor/transformer | Not started | Build gradually |
| Semiconductor stress/loss | Not started | MOSFET/diode first |
| Gate drive and dead time | Not started | Buck synchronous stage then bridges |
| Sensing circuits | Not started | Voltage/current sampling |
| Protection hardware | Not started | OVP/OCP/SCP/OTP, comparators |
| PCB layout for power converters | Not started | Hot loop, ground, sensing path |
| Thermal design | Not started | Loss and derating later |
| EMI/EMC awareness | Not started | Later hardware depth |
| PWM basics | Not started | Month 2 |
| ADC sampling sync | Not started | Month 2 |
| PI/PID control | Not started | Month 2 |
| Voltage/current loops | Not started | Month 2 |
| PSIM/PLECS | Not started | Early simulation tool |
| MATLAB/Simulink | Not started | Control-system support |
| TI C2000 ePWM | Not started | Digital control platform |
| TI C2000 ADC | Not started | Digital control platform |
| TI C2000 Trip Zone/CMPSS | Not started | Hardware-fast protection |
| CAN | Not started | Product/system integration |
| Real hardware power debugging | Not started | Low-voltage first |

## Known Strengths

- STM32 embedded development.
- Upper-computer development.
- CPLD experience.
- Control-board design.
- Communication ports and common protocols except CAN.

## Known Weaknesses To Revisit Often

- Power-stage topology intuition.
- Hardware sizing for power stages.
- Magnetics.
- Device stress, losses, thermal design.
- PCB layout for high-current/high-dvdt loops.
- Control-loop math and tuning.
- TI C2000/DSP specifics.
- Power debugging and safety.
- CAN in industrial/vehicle power products.

## Next Planned Topic

Buck converter basics:

- Function.
- Current paths.
- Duty-cycle relation.
- Inductor current waveform.
- Simple calculations.

## Planning Decision Rules

Use these rules after reviewing each daily note:

- Advance: The learner explains the concept correctly, completes exercises, and confidence is 4-5.
- Continue with light review: The learner is mostly correct but has one or two unclear points, confidence is 3.
- Slow down: The learner confuses current paths, formulas, control concepts, waveform meaning, or hardware stress.
- Add challenge: The learner completes more than planned or asks deeper questions; add a harder exercise or related next concept.
- Update this tracker when a topic or mastery gate is actually completed, even if it happens earlier or later than the roadmap.

## Mastery Gate Update Rules

For each topology:

- Principle can move to working depth after the learner can draw switching states, current paths, key waveforms, and explain CCM/DCM or equivalent operating modes.
- Hardware can move to working depth after the learner can size or justify main components, identify device stress, sensing, protection, thermal, and layout priorities.
- Simulation can move to working depth after the learner can build or explain a model and interpret normal/abnormal waveforms.
- Software/control can move to working depth after the learner can explain PWM/sampling/control/protection/state-machine strategy.
- Debug can move to working depth after the learner can define safe bring-up steps, measurement points, expected waveforms, and likely causes of abnormal waveforms.
