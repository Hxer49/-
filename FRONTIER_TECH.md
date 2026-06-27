# Frontier Technology Protocol

This file defines how frontier industry technology is included in the learning path.

## Core Rule

After each major topic, topology, or module reaches a usable foundation, Codex should guide the learner through a "traditional design vs frontier design" comparison.

The learner should first understand the classic design. Then add frontier awareness so the learner can understand modern industry direction without confusing fundamentals.

## Frontier Topics To Track

Track these themes throughout the roadmap:

- Wide-bandgap devices: GaN and SiC.
- High-frequency power conversion.
- Advanced gate drivers and protection.
- Advanced packaging and parasitic reduction.
- Planar magnetics and high-frequency magnetic design.
- Digital control and model-based control.
- Totem-pole PFC and bridgeless PFC.
- High-efficiency LLC, CLLC, and bidirectional resonant converters.
- Bidirectional DC/DC for battery, vehicle, and energy storage systems.
- High-voltage vehicle power: OBC, traction inverter, DC/DC.
- Data-center power architecture: 48V bus, intermediate bus converters, high-current POL.
- Solid-state transformers and modular power conversion awareness.
- EMI/EMC methods for high-dv/dt and high-di/dt designs.
- Thermal design for high power density.

## When To Add Frontier Content

Add frontier comparison at these points:

1. After basic Buck principle and hardware blocks are understood:
   - Compare silicon MOSFET Buck versus GaN high-frequency Buck.
2. After Boost and Buck-Boost:
   - Compare silicon Boost versus SiC/GaN Boost and bidirectional designs.
3. After PFC:
   - Compare diode bridge + Boost PFC versus totem-pole PFC using GaN/SiC.
4. After LLC/PSFB:
   - Compare classic LLC/PSFB versus high-frequency GaN/SiC implementations and planar magnetics.
5. After inverter:
   - Compare silicon IGBT/MOSFET inverter versus SiC traction inverter.
6. After real hardware/debug modules:
   - Discuss how high dv/dt, parasitics, probing, layout, and EMI become harder with GaN/SiC.

## Required Comparison Format

Use this format:

```text
Classic approach:
- Device/topology:
- Switching frequency:
- Advantages:
- Limitations:

Frontier approach:
- Device/topology:
- Why industry uses it:
- New design problems:
- Required new skills:

What to learn now:
- 
What to postpone:
- 
```

## Important Learning Boundary

Do not let frontier content replace fundamentals. GaN, SiC, advanced packaging, and high-frequency magnetics amplify the same core principles:

- current paths
- parasitic inductance/capacitance
- gate drive
- switching loss
- thermal design
- EMI
- sensing and protection
- control-loop behavior

The learner should learn enough frontier context to understand industry direction, then return to core mastery and projects.
