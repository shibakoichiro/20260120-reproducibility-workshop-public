# Reproducible Research Workflow Workshop

**Date**: January 20, 2026
**Duration**: 3 hours
**Audience**: Doctoral and master's students in public health/epidemiology

## Workshop Overview

Learn to build a reproducible research workflow from raw data to publication-ready manuscript using modern tools:

- **Quarto** for literate programming
- **gtsummary & ggplot2** for code-generated tables and figures
- **Git/GitHub** for version control
- **R functions & purrr** for DRY (Don't Repeat Yourself) coding

### Core Message

> "Reduce manual work and copy-paste by automating with code to achieve reproducibility"

## Workshop Materials

| Resource | Description |
|----------|-------------|
| Workshop Website | This repository is designed to be published via GitHub Pages (see the Actions workflow and repo Settings → Pages). |
| [Setup Guide](setup.qmd) | Pre-workshop installation instructions |
| [Slides](slides/slides.qmd) | Presentation slides |
| [Hands-on Exercises](parts/part1.qmd) | Step-by-step exercises |

## Workshop Structure

| Part | Topic | Time |
|------|-------|------|
| 1 | Why Reproducibility? | 10 min |
| 2 | Project Setup & Git | 15 min |
| 3 | Quarto Basics | 20 min |
| ☕ | Break | 10 min |
| 4 | DRY: Functions & purrr | 15 min |
| 5 | Tables & Figures + Git restore | 40 min |
| ☕ | Break | 10 min |
| 6 | Quarto Manuscripts & embed | 25 min |
| 7 | Word Collaboration | 20 min |
| 8 | Wrap-up: GitHub, targets, AI | 15 min |

## Repository Structure

```
├── index.qmd             # Website home page
├── setup.qmd             # Setup instructions
├── slides/               # Workshop slides (revealjs)
│   └── slides.qmd
├── parts/                # Hands-on exercise pages (Parts 1-8)
├── classroom-template/   # GitHub Classroom template for students
├── examples/             # Reference materials (manuscript example, bias analysis)
├── runthrough/           # Self-study reference project
└── docs/                 # Generated website (GitHub Pages)
```

## For Instructors

See `examples/nhanes-manuscript/` for example analysis files.

## License

[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

You are free to share and adapt these materials for any purpose, even commercially, as long as you give appropriate credit.

**Attribution:** Shiba K (2026). Reproducible Research Workflow Workshop Materials.
