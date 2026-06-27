# Daily TXT Export Protocol

Use this protocol whenever Codex prepares next-day detailed learning content.

## Export Directory

Default local export directory:

`C:\Users\rcrt\Desktop\HxWork\电源学习`

If the computer changes or the path is unavailable, ask the learner for the new export directory. The GitHub learning archive remains the portable source of truth.

## File Naming

Use this naming pattern:

`DayN_short-topic.txt`

Examples:

- `Day1_Buck基础1.txt`
- `Day2_Buck电流路径与波形.txt`
- `Day3_Buck分压与RC滤波.txt`

Rules:

- `N` is the learning day number, starting from 1.
- The short topic should describe the day's content.
- Keep the name short enough to scan in a folder.
- Prefer `.txt` for easy opening on any computer.

## Required Content

The TXT file should contain the same practical learning package as `tomorrow-plan.md`:

1. Study time.
2. Topic.
3. Current gate.
4. Learning mode.
5. Learning objectives.
6. Pre-study review.
7. Concrete knowledge points.
8. Hands-on tasks.
9. What the learner should submit.
10. Codex assessment questions.
11. Passing criteria.
12. Notes about frontier technology, if relevant.

## Update Rule

When Codex generates tomorrow's concrete content:

1. Update `tomorrow-plan.md`.
2. Export the same content as a standalone TXT file in the export directory.
3. Use the next Day number unless the learner explicitly asks to overwrite.
4. Mention the saved TXT path in the final response.

## Important

Do not rely on the desktop TXT files as the only long-term record. They are convenient study handouts. The markdown archive and GitHub repository remain the long-term source of truth.
