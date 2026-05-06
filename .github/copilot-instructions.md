# Rotura Math Skills — GitHub Copilot Instructions

This project contains three math processing skills. Each skill reads from `input/` and writes to `output/`.

## Available Prompts

Reference these in Copilot Chat using `#<filename>`:

| Prompt file | What it does |
|---|---|
| `#normalize-problem.prompt.md` | Normalize a math problem and classify its domain |
| `#evaluate-responses.prompt.md` | Evaluate model responses against a ground truth solution |
| `#format-solution.prompt.md` | Reformat a solution to meet submission requirements |

## File Conventions

- Input files live in `input/`
- Output files go to `output/`
- Never modify `SAMPLE_WORKSPACE/`
