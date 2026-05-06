# Skill 2 — Math Response Evaluator

Evaluate model responses against a ground truth solution. Process each response as a separate todo — do not read both response files at the same time.

## Files

| File | Description |
|---|---|
| `input/problem.md` | The original math problem |
| `input/solution.md` | Ground truth answer in LaTeX |
| `input/response1.md` | First model response to evaluate |
| `input/response2.md` | Second model response to evaluate |

---

## Todo 1 — Evaluate response1.md

**Read in order:**
1. `input/problem.md`
2. `input/solution.md`
3. `input/response1.md`

**Evaluate:**
- Is the final answer mathematically equivalent to `solution.md`?
- Is the reasoning correct at each step? Identify any step that is wrong, skipped, or unjustified.

**Write** `output/response1_check.md` using the output format below.

---

## Todo 2 — Evaluate response2.md

**Read in order:**
1. `input/problem.md`
2. `input/solution.md`
3. `input/response2.md`

**Evaluate:** same criteria as Todo 1.

**Write** `output/response2_check.md` using the output format below.

---

## Output format

Put the verdict block **first**, then the detailed breakdown.

```markdown
# Response Evaluation

## Verdict

| Field | Value |
|---|---|
| **Result** | ✅ Correct / ❌ Incorrect / ⚠️ Partially correct |
| **Answer match** | ✅ Matches ground truth / ❌ Does not match / ⚠️ Equivalent but different form |
| **Reasoning** | ✅ Valid / ❌ Contains errors / ⚠️ Gaps present |

---

## Answer Comparison

**Ground truth:** {final answer from solution.md}

**Response answer:** {final answer from response}

{Explain whether they are mathematically equivalent and why.}

---

## Step-by-step Review

{For each major step in the response, write one short paragraph:
- What the step claims
- Whether it is correct
- If wrong or incomplete: explain the exact issue}

---

## Issues Found

{List only actual problems. If none, write "None." Each issue should state:
- Where it occurs (e.g. "Step 3", "Final simplification")
- What is wrong
- What the correct approach should be}
```
