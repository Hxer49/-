# Tomorrow Plan

Date planned: 2026-06-29
Study duration: 2 hours
Topic: Buck converter basics, with hardware/software/analog support perspective

## Goal

Understand what a Buck converter does, how current flows during MOS on/off states, why the ideal relationship is `Vout = D * Vin`, what the main hardware blocks are, and why basic analog circuits are needed for sensing.

## Schedule

| Time | Task | Output |
|---:|---|---|
| 0-15 min | Understand Buck as a step-down DC/DC converter | One-sentence definition |
| 15-40 min | Study MOS on-state and off-state current paths | Two current-path sketches |
| 40-55 min | Learn ideal duty-cycle relation | Memorize `Vout = D * Vin` |
| 55-75 min | Draw key waveforms | Inductor current, PWM, output voltage |
| 75-95 min | Identify hardware blocks | MOS/diode or sync MOS/inductor/capacitor/driver/sampling |
| 95-110 min | Analog entry: resistor divider and RC filter | Explain why ADC cannot directly sample high output voltage |
| 110-115 min | Do duty-cycle exercises | Three calculated answers |
| 115-120 min | Write daily log | Add entry to `daily-log.md` |

## Must-Know Points

1. Buck is a step-down converter.
2. During MOS on-time, input energy goes to the inductor, capacitor, and load.
3. During MOS off-time, the inductor continues supplying the load through a diode or synchronous MOS path.
4. In ideal continuous conduction mode, `Vout = D * Vin`.
5. Inductor current is a ripple waveform, not a fixed DC line.
6. Buck hardware is not only MOS + inductor; it also needs drive, sensing, protection, layout, and thermal thinking.
7. A digital controller needs analog front-end circuits to scale, filter, and protect ADC inputs.

## Exercises

1. `Vin = 24V`, target `Vout = 12V`: calculate duty cycle.
2. `Vin = 48V`, target `Vout = 12V`: calculate duty cycle.
3. `Vin = 60V`, `D = 0.2`: calculate ideal output voltage.

## Send Back To Codex

After studying, send your notes and any artifact you created. Codex will evaluate whether the Buck principle gate is still `Learning` or can move toward `Working depth`.

```text
1. Buck function:
2. Current path when MOS is on:
3. Current path when MOS is off:
4. Duty-cycle formula:
5. Main hardware blocks:
6. Why Buck voltage sensing needs a resistor divider/RC filter:
7. Answers to the three exercises:
8. Sketch/photo/simulation/code if available:
9. Questions I still have:
```

Assessment rule:

- Do not mark yourself as passed.
- Codex will review the evidence, ask follow-up questions if needed, then decide the current level.
