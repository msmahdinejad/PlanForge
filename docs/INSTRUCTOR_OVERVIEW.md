# Instructor Overview

PlanForge is a constraint satisfaction project for an Artificial Intelligence fundamentals course. Students receive a visual apartment-planning studio and implement the CSP solver logic inside `student/`.

## Public Package

The repository intentionally contains only the public assignment surface:

- `planforge/core/`: framework code for loading problems, building domains, validating layouts, scoring architectural quality, and rendering the desktop UI.
- `planforge/examples/`: visible JSON cases covering easy, medium, hard, unsatisfiable, and bonus stress-test scenarios.
- `planforge/grader/`: public self-check wrapper and compiled binaries for supported Python/OS combinations.
- `student/`: starter files with explicit TODOs for the solver, consistency checks, heuristics, inference, and soft scoring.
- `docs/PlanForge_Technical_Report.pdf`: the English technical report generated from LaTeX.

## Private Material Policy

Private grading scripts, hidden tests, batch grading reports, and reference-solution source files are not included in this public repository. The public grader is only a self-check; final grading should be performed with a separate private grader and hidden cases.

## Grading Shape

The project is structured around 100 required points and 30 optional/bonus points:

- Required: recursive backtracking, completeness detection, hard-constraint consistency, MRV, LCV, valid layouts for public examples, unsatisfiable-case detection, and instrumentation calls.
- Optional: forward checking, AC-3, stronger pruning, multi-solution search, and meaningful soft scoring for higher-quality floor plans.

## Recommended Release Workflow

Before distributing the project:

1. Run `python -m compileall planforge student`.
2. Run `python run_app.py` and manually verify that the visualizer opens.
3. Run `python run_public_grade.py` with the reference solution package, not the starter package.
4. Rebuild `docs/PlanForge_Technical_Report.pdf` from `docs/PlanForge_Technical_Report.tex` if documentation changes.
5. Confirm that no private grader, hidden cases, reference solution code, or batch grading reports are present in the public repository.
