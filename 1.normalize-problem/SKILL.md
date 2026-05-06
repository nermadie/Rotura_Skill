# Math Problem Normalizer

Read `input/problem.md`, process the math problem, write result to `output/problem.md`.

## Task

1. **Normalize LaTeX** — rewrite the problem in clean, standard LaTeX. Use `$...$` for inline math, `$$...$$` for display equations. Replace any Unicode math symbols with proper LaTeX commands. Keep the problem complete and self-contained.

2. **Classify domain and sub-domain** — choose from the taxonomy below.

3. **Write domain explanation** — 3–5 sentences following this structure:
   - "This problem involves [key elements], which are part of [domain and subdomain]."
   - "The problem also involves [additional elements], which are part of [other domain]."
   - "However, [why the primary domain is more fundamental or advanced]."

## Domain Taxonomy

| Domain | Sub-domains |
|---|---|
| Abstract Algebra | Ring theory, Group theory, Module theory, Field theory, Representation theory, Galois theory |
| Discrete Mathematics and Combinatorics | Enumerative combinatorics, Generating functions, Probabilistic combinatorics |
| Probability and Statistics | Stochastic processes, Probability foundations, Random variables and distributions, Bayesian statistics, Statistical inference, Limit theorems |
| Calculus | Integral calculus, Multivariable calculus, Differential calculus, Infinite sequences and series, Single-variable calculus, Vector calculus |
| Number Theory | Algebraic number theory, Modular arithmetic and congruences, Analytic number theory, Elementary number theory, Diophantine equations |
| Analysis | Functional analysis, Real analysis, Complex analysis, Fourier analysis, Measure theory, Asymptotic analysis |
| Optimization and Numerical Mathematics | Convex optimization, Nonlinear optimization, Discrete optimization, Approximation theory, Numerical analysis, Error analysis and stability |
| Linear Algebra | Linear operators, Matrix decompositions and canonical forms, Spectral theory, Finite-dimensional linear algebra, Inner product spaces, Numerical linear algebra |
| Differential Equations and Dynamical Systems | Dynamical systems, Ordinary differential equations, Bifurcation theory, Boundary value problems, Partial differential equations, Stability theory |
| Geometry and Topology | Riemannian geometry, Point-set topology |
| Logic and Foundations | Computability, Set theory, Model theory, Mathematical logic, Proof theory |

## Output format (`output/problem.md`)

```markdown
# Normalized Math Problem

## LaTeX (Normalized)

{latex}

---

## Domain Classification

| Field | Value |
|---|---|
| **Domain** | {domain} |
| **Sub-domain** | {subdomain} |

---

## Domain Explanation

{explanation}
```