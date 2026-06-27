# Digital Power Learning Profile

## Learner

- Goal: Become proficient, then expert-level, in power electronics and digital power full-stack engineering over a multi-year learning path.
- Target depth: Master the major power topologies from both hardware and software perspectives, not only write control software.
- Daily study time: Usually about 2 hours, but holiday/free-day study time can be longer or shorter.
- Preferred workflow: Ask Codex for the next day's plan, study, then report notes/questions for the next plan.
- Current date when profile started: 2026-06-28.

## Current Background

- Has practical STM32 development experience.
- Has upper-computer/PC tool development experience.
- Has CPLD experience.
- Has designed control boards.
- Familiar with communication ports except CAN.
- Familiar with common communication protocols.
- Has little analog circuit foundation. Analog electronics must be built into the long-term plan from the beginning.

## Target Roles

- Digital power software engineer.
- Power supply software engineer.
- Senior power supply software engineer.
- Power electronics hardware/software full-stack engineer.
- Digital power control and topology design engineer.

## Main Skill Gaps

- Power electronics topology knowledge and design: Buck, Boost, Buck-Boost, synchronous Buck/Boost, bidirectional DC/DC, flyback, forward, push-pull, half bridge, full bridge, phase-shift full bridge, LLC, PFC, rectifier, inverter.
- Analog circuit foundation: resistor/capacitor behavior, RC filters, diodes, BJTs/MOSFET small-signal basics, op-amps, comparators, feedback, compensation, noise, grounding, sampling front ends.
- Hardware design for each topology: device selection, magnetic components, capacitor selection, drive circuit, sampling circuit, protection circuit, thermal design, layout, efficiency, EMI awareness.
- Digital power control: PWM/ADC timing, voltage loop, current loop, PI/PID, soft start, protection logic, loop stability.
- TI C2000/DSP ecosystem: ePWM, ADC trigger, CMPSS, Trip Zone, CLA, HRPWM, CCS.
- Simulation: PSIM, PLECS, MATLAB/Simulink.
- CAN communication and, later, CANopen/J1939/UDS basics if vehicle power roles require it.
- Power-stage debugging: oscilloscope waveforms, electronic load testing, overcurrent/overvoltage behavior, noise, dead time, device protection.
- Engineering workflow: reading datasheets/application notes, deriving requirements, creating design documents, BOM awareness, derating, reliability, safety, test plans, and version-controlled project records.

## Long-Term Definition Of "Expert"

Expert-level does not mean only knowing theory. It means being able to:

- Explain common power topologies, current paths, key waveforms, and control goals.
- For each major topology, explain the operating modes, stress, key waveforms, failure modes, and practical design tradeoffs.
- Design the hardware around each topology at a reasonable engineering level: switches, magnetics, capacitors, drivers, sensing, protection, thermal path, and PCB layout priorities.
- Design and debug the analog support circuits around power stages: voltage/current sensing, filters, op-amp conditioning, comparators, references, protection thresholds, compensation networks, and noise/grounding issues.
- Build and tune closed-loop digital control for representative DC/DC and DC/AC/AC/DC systems.
- Use simulation to validate topology behavior, hardware sizing, and control-loop response.
- Implement robust embedded software on STM32 and TI C2000/DSP.
- Design product-like software architecture: state machine, faults, protection, parameters, communication, logging, calibration, upgrades.
- Debug real hardware safely with power instruments.
- Analyze unstable output, overshoot, protection trips, sampling noise, PWM timing problems, and hardware/software interaction problems.
- Write clear project documentation and explain the work in interviews.
- Convert product requirements into electrical/software requirements, test plans, fault tables, and design-review material.
- Work safely with power hardware, including current limiting, isolation awareness, discharge checks, and instrument setup.

## Topology Mastery Standard

For every major topology, mastery means passing these gates:

1. Principle gate: draw the topology, current paths, switching states, and key waveforms.
2. Hardware gate: calculate or select main devices and explain voltage/current stress, losses, sensing, protection, thermal, and layout priorities.
3. Simulation gate: build an open-loop and, when applicable, closed-loop simulation and explain the waveforms.
4. Software/control gate: describe or implement PWM strategy, sampling strategy, control loop, soft start, protection, and state machine.
5. Debug gate: know what to measure, expected oscilloscope waveforms, common abnormal waveforms, and likely causes.
6. Analog support gate, when relevant: explain sensing, filtering, op-amp/comparator behavior, reference/threshold design, noise path, and grounding/layout effect.

Important: Do not require full product-level depth before moving to the next topology. First reach engineering working depth, then revisit product-level details through projects and debugging cases.

## Daily Planning Rules

When asked for tomorrow's plan:

- Read this file, `progress-tracker.md`, `daily-log.md`, and `tomorrow-plan.md` if available.
- Default to a 2-hour plan unless the learner says tomorrow has more or less available time.
- Treat the roadmap as a direction, not a fixed calendar.
- Use the learner's newest notes as the source of truth for actual progress.
- If the learner mastered more than expected, compress or skip already-mastered review and move forward.
- If the learner is stuck, slow down and add review, examples, and smaller exercises.
- If the learner studied extra during a holiday, update progress based on demonstrated notes, not on the original daily plan.
- Include review, new learning, hands-on practice, and a concrete output.
- Prefer one clear topic per day.
- Avoid overloading the day with too many concepts.
- Include 3-5 small exercises or checkpoints.
- End with exactly what the learner should send back after studying.

## Long-Term Continuity Rules

- Important progress must be written to the archive files, not only remembered in chat.
- The archive directory should be portable to another computer.
- If the path changes after migration, Codex should first locate the archive files in the current project before relying on the old absolute path.
- The personal skill is helpful but not the only source of truth; the archive files are the source of truth.
- When changing computers, copy this entire `digital-power-learning` directory and, if possible, copy or recreate the `digital-power-coach` skill.

## Current Starting Point

The first learning topic is Buck converter basics:

- What Buck does.
- MOS on/off current paths.
- Ideal duty-cycle relation: Vout = D * Vin.
- Inductor current waveform.
- Simple duty-cycle calculations.
