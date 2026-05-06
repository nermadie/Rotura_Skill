# Rotura Math Skills — Gemini System Instructions

This project contains three math processing skills. Each skill reads from `input/` and writes to `output/`. Prompt files for each skill are in `.gemini/`.

## Skills

| Prompt file | Skill name | Description |
|---|---|---|
| `.gemini/normalize-problem.md` | Math Problem Normalizer | Normalize a math problem in LaTeX and classify its domain |
| `.gemini/evaluate-responses.md` | Math Response Evaluator | Evaluate model responses against a ground truth solution |
| `.gemini/format-solution.md` | Solution Formatter | Reformat a solution to meet submission requirements |

## Usage

Load a skill prompt with:
```
gemini -p "$(cat .gemini/normalize-problem.md)"
gemini -p "$(cat .gemini/evaluate-responses.md)"
gemini -p "$(cat .gemini/format-solution.md)"
```

Or paste the contents of the relevant prompt file as your system prompt before running.
