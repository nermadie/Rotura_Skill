---
agent: agent
description: Reformat a math solution to meet submission requirements
---

Read `input/solution.md`, reformat it to meet submission requirements, write to `output/solution.md`.

---

## Rules
- Normalize the LaTeX syntax: fix any non-standard or shorthand commands to use only basic LaTeX syntax. Do **not** change the mathematical content or style of writing — only fix syntax.
  - e.g. `\Z` → `\mathbb{Z}`, `\abs{x}` → `|x|`, `\norm{x}` → `\|x\|`, `\d` → `dx`, mismatched brackets, missing `\left`/`\right`, etc.

### Steps
- Each step must make a **substantial advance** toward the final answer — do not split into trivial micro-steps
- Every step starts with `Step N:` (e.g. `Step 1:`, `Step 2:`)
- The **final step** must end with: `Final Answer: $\boxed{<answer>}$`

### Answer field
- Wrap the final answer in `$...$`
- Do **not** use `\boxed`

### Problem Type — pick the **one** that best describes the problem
- `Exact computation` — asks for an exact numerical value or mathematical object
- `Symbolic derivation` — asks for a closed-form expression, identity, recurrence, transform, or asymptotic form
- `Numerical approximation` — asks for a numerical answer to a specified tolerance or precision
- `Solve for unknowns` — asks for values/objects satisfying an equation or condition
- `Construction under constraints` — asks for any valid object satisfying structural/quantitative constraints
- `Optimization` — asks for an optimal value, optimizer, or both
- `Classification by exhaustive solution set` — asks for the complete set of all valid solutions
- `Canonicalization or normalization` — asks for an object in a specified standard or reduced form
- `Transformation between representations` — asks for conversion between mathematically equivalent representations
- `Parameter identification` — asks for unknown parameters or coefficients inferred from equations or structure

### Answer Type — pick all that apply
- `Exact scalar` — single exact quantity (integer, rational, algebraic number, closed-form constant)
- `Numerical scalar approximation` — single numerical quantity to a specified tolerance
- `Exact symbolic expression` — closed-form symbolic expression, correct up to mathematical equivalence
- `Polynomial or rational function` — polynomial or rational function in symbolic form
- `Vector` — finite-dimensional vector as coordinates or components
- `Matrix` — matrix with exact or numerical entries
- `Set or multiset of objects` — complete finite collection of valid outputs
- `Sequence or series representation` — sequence, recurrence, or series-form representation
- `Canonical form` — object in a specified standard form (diagonal, Jordan, RREF, etc.)
- `Constructed mathematical object` — explicitly given object satisfying constraints (multiple correct answers may exist)
- `Geometric object or description` — geometric entity or characterization (curve, region, surface, transformation)

---

## Output format (`output/solution.md`)

```markdown
## Steps

Step 1:
{first major step}

Step 2:
{second major step}

...

Step N:
{final step}

Final Answer: $\boxed{<answer>}$

---

## Answer

$<normalized answer without \boxed>$

---

## Classification

**Problem Type:** {single best-fit type}

**Answer Type:** {comma-separated list of applicable types}
```
