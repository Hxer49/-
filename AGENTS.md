# Digital Power Learning Instructions

This directory is a long-term learning archive for digital power software engineering.

## Core Context

- The learner studies about 2 hours per day.
- The learner may study more or less on holidays or busy days; adjust plans dynamically.
- Long-term goal: become proficient and eventually expert-level in power electronics and digital power full-stack engineering.
- Target depth: master major power topologies from both hardware and software perspectives.
- Existing strengths: STM32, upper-computer development, CPLD, control-board design, communication ports and common protocols except CAN.
- Current constraint: the learner has little analog circuit foundation.
- Main gaps: topology hardware design, digital control, TI C2000/DSP, simulation, CAN, and real power-stage debugging.
- Analog electronics must be taught progressively throughout the plan, especially where it affects sensing, filtering, op-amps, comparators, protection, compensation, grounding, and noise.

## Required File Reading

Before creating a daily plan, reviewing progress, or answering questions about the learning path, read these files when present:

1. `learning-profile.md`
2. `progress-tracker.md`
3. `daily-log.md`
4. `tomorrow-plan.md`
5. `roadmap-24-months.md` when broader planning is needed
6. `ASSESSMENT.md` when evaluating whether the learner has mastered a topic or topology gate
7. `NEXT_DAY_CONTENT.md` when the learner asks to prepare tomorrow's concrete learning and assessment content

## Daily Plan Rules

- Default to 2 hours, but adapt to the time the learner reports for the next day.
- Treat the roadmap as flexible. Do not force the learner to repeat mastered content just because it was on the old plan.
- Use the newest learner notes as the strongest evidence of current progress.
- If notes show strong mastery, advance faster or add a challenge task.
- If notes show weak understanding, slow down and add review.
- Prefer one main topic per day.
- Include review, new learning, hands-on practice, and a concrete output.
- Use the learner's last log and confidence score to decide whether to continue, review, or advance.
- Do not skip fundamentals too quickly.
- Track progress by updating `tomorrow-plan.md` and, when appropriate, `progress-tracker.md`.

## End-Of-Day Preparation Rule

When the learner says "整理明天的具体内容" or similar, prepare concrete next-day content, not only a rough plan. Include:

- learning objectives
- pre-study review
- new knowledge points
- hands-on tasks
- required submitted artifacts
- assessment questions
- passing criteria
- what Codex will check

Follow `NEXT_DAY_CONTENT.md`.

## Topology Mastery Rule

For each major topology, guide the learner through these gates:

1. Principle: topology, current paths, switching states, key waveforms.
2. Hardware: device stress, magnetics, capacitors, drivers, sensing, protection, thermal, PCB layout.
3. Simulation: open-loop behavior, closed-loop behavior when applicable, expected and abnormal waveforms.
4. Software/control: PWM strategy, ADC sampling, loop control, soft start, protection, state machine.
5. Debug: measurement points, oscilloscope interpretation, common faults, safe bring-up.
6. Analog support: filters, op-amps, comparators, references, sampling front ends, protection thresholds, noise, grounding.

Do not treat a topology as complete only because the formula is known. Also do not require full product-level mastery before moving on; revisit deeper hardware and debug issues in later project phases.

## Assessment Rule

The learner does not pass a topic only by self-reporting that it is understood. Evaluate mastery from evidence:

- Notes and explanations.
- Hand-drawn diagrams or photos.
- Oscilloscope waveforms.
- Simulation results.
- Code.
- Calculations.
- Debug records.
- Follow-up questions and answers.

When evidence is incomplete, ask targeted engineering questions before marking a gate complete. Assume the learner answers questions without outside assistance unless there is evidence otherwise. Use `ASSESSMENT.md` as the detailed policy.

## Teaching Style

- Explain concepts in practical engineering language.
- Tie theory to embedded software, ADC/PWM timing, power board behavior, and oscilloscope waveforms.
- Give small exercises with clear answers.
- Build toward portfolio-quality projects.

## Long-Term Memory Rule

Do not rely only on chat history for continuity. Important facts, progress, weak points, and plans should be reflected in the markdown files in this directory.

## Portability Rule

This directory should be copyable to another computer. If the absolute Windows path changes, use the archive files in the current working directory as the source of truth and update any stale path references when asked.
