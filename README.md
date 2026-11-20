# Project Kumar Azad · Research Workspace 2026–2028

A public, version-controlled workspace for exploratory work in **theoretical and mathematical physics, Mathematica-based symbolic mathematics, AI for scientific computing, and quantum computing**.

**Open the research workspace:** https://krazad0.github.io/research-workspace/

**Source repository:** https://github.com/KrAzad0/PROJECT-KUMAR-AZAD-2026-2028

> Research integrity: project cards describe current questions and intended checks. The presence of a card does **not** mean that the calculation is complete, numerically validated, novel, accepted for publication, or experimentally realized.

## What is in this repository?

| File | Purpose |
| --- | --- |
| [`workspace/projects.json`](workspace/projects.json) | Single editable registry for all project cards, statuses, planned steps, milestones and dated updates |
| [`index.html`](index.html) | Standalone responsive dashboard; can also be served through this repository's own GitHub Pages, if enabled |
| `README.md` | How to update the workspace and publish research evidence |

The personal website hosts an additional [dashboard page](https://krazad0.github.io/research-workspace/), which reads `workspace/projects.json` from this repository. Updates committed to `main` become visible after the public raw-file cache refreshes. Until then, the page may display an older snapshot.

## How to update an ongoing project

1. Open **[Edit projects.json](https://github.com/KrAzad0/PROJECT-KUMAR-AZAD-2026-2028/edit/main/workspace/projects.json)** on GitHub and sign in.
2. Locate the relevant object in the `projects` array by its unique `id`.
3. Change `status`, `phase`, `question`, `summary`, `next_step`, `validation`, `methods` or `links`. Valid existing status terms include `In development`, `Scoping`, `Study` and `Idea`; use clear language and do not imply results that have not been verified.
4. Append a dated entry in `updates` when a meaningful change or reproducible result occurs.
5. Set the top-level `updated` field to the change date in `YYYY-MM-DD` format, validate that the JSON is syntactically correct, and commit to `main`.
6. Reopen the [research workspace](https://krazad0.github.io/research-workspace/). The page is read-only; editing takes place on GitHub, not through the website.

### Example dated log entry

```json
{
  "date": "2026-11-20",
  "title": "Baseline validation planned",
  "note": "Defined the test Hamiltonian, units and numerical convergence criteria. Numerical results are not yet verified."
}
```

Only add claims of completed calculations after you have checked them against a reproducible code/notebook and independent limits. Link the resulting source, plot, technical report, or preprint from the project's `links` array when those artifacts actually exist.

## Proposed research directory convention

As individual projects mature, store their materials under folders matching the project identifier:

```text
projects/
  toroidal-hydrogen/
    README.md
    theory/
    notebooks/
    matlab/
    results/
  symbolic-quantum-mathematica/
    README.md
    notebooks/
  ai-for-physics/
    README.md
    python/
  quantum-computing/
    README.md
    notebooks/
```

These folders are **suggestions** for future project files, not a claim that the code or results are already present. Use `results/` only for verifiable outputs. Put assumptions, equations, parameter values, environment information, dependency versions, and numerical convergence criteria in each project's README.

## Research workflow

**Question → literature → assumptions → mathematical model → baseline → code/notebook → convergence and physical checks → documented result.**

For the exploratory hydrogen-in-a-solid-torus model, define a **three-dimensional solid torus**, the nuclear position, a self-adjoint boundary-value problem, the external pulse and physically meaningful observables before interpreting numerical dynamics. A prescribed attosecond field is not automatically a uniform physical field filling the volume; electromagnetic modeling assumptions must be stated.

## Maintaining the dashboard

- The dashboard code is in `index.html` here and mirrored on the personal GitHub Pages repository under `research-workspace/index.html`.
- The **data source of truth** remains `workspace/projects.json` in this repository.
- The website uses plain HTML, CSS and browser JavaScript; it does not request GitHub credentials or write to the repository from a visitor's browser.
- To add a new project, copy a project object in the JSON, use a distinct `id`, choose one of the declared tracks, provide a specific scientific question, and include a checkable next step.
- If a repository, notebook or paper is not public, omit the link rather than inventing one.

## Licence and contact

This repository is an ongoing personal research archive. Unless a separate licence is added, do not assume the contents are broadly licensed for reuse. Contact links are available on [Kumar Azad's personal webpage](https://krazad0.github.io/).
