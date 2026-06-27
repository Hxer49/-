# Evidence-Based Mastery Assessment

This file defines how Codex should evaluate whether the learner has actually mastered a topic or topology gate.

## Core Rule

The learner does not pass a topic only by saying "I understand" or "I finished." Codex must judge mastery from evidence.

Evidence can include:

- Written notes.
- Hand-drawn diagrams or photos of diagrams.
- Oscilloscope waveforms or screenshots.
- Simulation schematics and results.
- Code written by the learner.
- Calculation sheets.
- Debug records.
- Dialogue with Codex.
- Oral-style answers typed by the learner.

Assume the learner answers Codex's assessment questions without using outside assistance unless there is evidence otherwise.

## Evidence Priority

Use this priority order when evaluating:

1. Working artifact evidence: code, simulation file/results, measured waveforms, calculation sheets.
2. Explanation evidence: notes, diagrams, typed answers, design reasoning.
3. Interactive questioning: Codex asks follow-up questions to check understanding.
4. Self-report: useful for confidence and learning preference, but not enough for passing.

If an artifact cannot be fully recognized from an image or file, ask the learner to describe key values, waveforms, test conditions, or code behavior. Then judge using the artifact plus the conversation.

## Assessment Workflow

When the learner submits notes, waveforms, code, simulation results, or asks whether they passed:

1. Identify which topology and mastery gate is being assessed:
   - Principle
   - Hardware
   - Simulation
   - Software/control
   - Debug
   - Frontier awareness, after the classic foundation is strong enough
2. Review the submitted evidence.
3. Mark what is correct, incomplete, unclear, or wrong.
4. Ask 2-5 targeted questions when the evidence is insufficient or when understanding needs verification.
5. Judge the learner's level after the answer.
6. Update the next plan based on the weakest important gap.

Do not ask trivia questions. Ask questions that reveal engineering understanding.

## Mastery Levels

Use these levels in `progress-tracker.md`:

| Level | Meaning |
|---|---|
| Not started | No meaningful evidence yet |
| Learning | Some correct understanding, but gaps remain |
| Working depth | Can explain and apply the concept in normal engineering situations |
| Project depth | Can implement, simulate, measure, or debug it in a project-like context |
| Review later | Good enough to move on, but needs future reinforcement |

## Passing Criteria By Gate

### Principle Gate

Pass to working depth when the learner can:

- Draw or describe the topology.
- Explain each switching state.
- Explain current paths.
- Sketch or interpret key waveforms.
- Explain main formula relationships and limits.
- Answer "what changes when load/input/duty changes?"

### Hardware Gate

Pass to working depth when the learner can:

- Identify main power components and their roles.
- Estimate or justify voltage/current stress.
- Explain inductor/transformer and capacitor selection basics.
- Explain MOSFET/diode/driver choices.
- Explain sensing and protection points.
- Identify thermal and PCB layout priorities.

### Simulation Gate

Pass to working depth when the learner can:

- Build or clearly interpret a simulation.
- Explain why the waveforms look correct.
- Change at least one parameter and predict the effect.
- Recognize abnormal waveforms and likely causes.

### Software/Control Gate

Pass to working depth when the learner can:

- Explain PWM strategy.
- Explain ADC sampling timing.
- Write or explain control-loop pseudocode.
- Explain soft start and protection handling.
- Explain state-machine behavior.
- Identify timing and saturation problems.

### Debug Gate

Pass to working depth when the learner can:

- Define safe bring-up steps.
- Identify measurement points.
- Predict expected waveforms.
- Interpret abnormal waveforms.
- Suggest likely causes and next measurements.

### Frontier Awareness Gate

Pass to working depth when the learner can:

- Compare a classic implementation with a modern frontier implementation.
- Explain why industry uses the frontier approach.
- Identify new design challenges introduced by the frontier approach.
- Explain which fundamentals remain the same.
- Name what should be learned now and what should be postponed.

## Questioning Strategy

Ask questions in layers:

1. Recall: "What is the current path when the switch is off?"
2. Reasoning: "Why does inductor current slope down in this interval?"
3. Application: "If Vin rises but duty is unchanged, what happens?"
4. Debug: "If the switch node rings heavily, what would you check?"
5. Design: "How would you choose the inductor ripple target?"

If the learner answers well, advance or add challenge work. If the learner answers partially, give targeted repair practice. If the learner answers incorrectly, slow down and rebuild the concept.

## Assessment Output Format

When evaluating a submission, Codex should respond with:

```text
Assessment:
- Gate:
- Evidence reviewed:
- What is correct:
- Gaps or risks:
- Follow-up questions:
- Current level:
- Next action:
```

When updating progress, record evidence briefly in `daily-log.md` and update the relevant cell in `progress-tracker.md`.
