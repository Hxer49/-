# Digital Power Learning Profile

## Learner

- Goal: Become proficient, then expert-level, in digital power software engineering over a multi-year learning path.
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

## Target Roles

- Digital power software engineer.
- Power supply software engineer.
- Senior power supply software engineer.

## Main Skill Gaps

- Power electronics topology knowledge: Buck, Boost, Buck-Boost, half bridge, full bridge, LLC, PFC, rectifier, inverter.
- Digital power control: PWM/ADC timing, voltage loop, current loop, PI/PID, soft start, protection logic, loop stability.
- TI C2000/DSP ecosystem: ePWM, ADC trigger, CMPSS, Trip Zone, CLA, HRPWM, CCS.
- Simulation: PSIM, PLECS, MATLAB/Simulink.
- CAN communication and, later, CANopen/J1939/UDS basics if vehicle power roles require it.
- Power-stage debugging: oscilloscope waveforms, electronic load testing, overcurrent/overvoltage behavior, noise, dead time, device protection.

## Long-Term Definition Of "Expert"

Expert-level does not mean only knowing theory. It means being able to:

- Explain common power topologies, current paths, key waveforms, and control goals.
- Build and tune closed-loop digital control for at least Buck and Boost converters.
- Use simulation to validate topology behavior and control-loop response.
- Implement robust embedded software on STM32 and TI C2000/DSP.
- Design product-like software architecture: state machine, faults, protection, parameters, communication, logging, calibration, upgrades.
- Debug real hardware safely with power instruments.
- Analyze unstable output, overshoot, protection trips, sampling noise, PWM timing problems, and hardware/software interaction problems.
- Write clear project documentation and explain the work in interviews.

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
