# Nastri CV

Source for Nico Nastri's academic CV, based on the [autoCV](https://github.com/jitinnair1/autoCV) LaTeX template.

## How this is published

Every push to `main` triggers `.github/workflows/deploy.yml`, which:
1. Compiles `cv.tex` (via `latexmk`, including a `biber` pass for the `citations.bib` bibliography)
2. Publishes the resulting PDF to GitHub Pages

Because this repo lives under the `ngnastri10` account, whose user site (`ngnastri10.github.io`) has the custom domain `niconastri.com`, this project's Pages deployment is served at:

**https://niconastri.com/Nastri-CV-2026/**

## Editing locally

- Requires a LaTeX distribution (e.g. [MiKTeX](https://miktex.org/)) with `biblatex`/`biber` support.
- `make` compiles `cv.pdf` locally via `latexmk` (same command the Action runs).
- `make clean` / `make distclean` remove build artifacts.
