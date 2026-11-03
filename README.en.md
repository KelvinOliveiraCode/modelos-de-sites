# modelos-de-sites

**English** · [Português (Brasil)](README.md)

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](#) [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](#) [![Vanilla JS](https://img.shields.io/badge/Vanilla%20JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](#) [![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-222?style=flat-square&logo=githubpages)](#)

## What it is

A **showcase of 20 landing pages**, one per niche (gym, law, medical clinic, real estate, pet shop, e-commerce, etc.), with a hub in `index.html` that navigates among the models. It serves as a portfolio of website-building work and as a ready base for a client to pick their segment.

## Status

In production. Published at <https://kelvinoliveiracode.github.io/modelos-de-sites/> (HTTP 200 verified).

## Features

- **Hub** (`index.html`) that lists and navigates to the 20 niche models.
- **20 individual landing pages**, each in its own folder with its own self-contained `index.html`.
- **Centralized design system** defined in `DESIGN.md` (the source of truth for all models' styling).
- **Build specs** in `spec/` (niches, landing rules, layout and visual review).

## Architecture

Each niche is a folder with an independent HTML page; the hub aggregates them. No build, no framework, no dependencies: only static HTML/CSS/JS.

```mermaid
flowchart LR
    H[hub index.html] --> A[academia-fitness]
    H --> M[moda-ecommerce]
    H --> P[pet-shop-vet]
    H --> ... [...20 niches]
    D[DESIGN.md - design system] -.-> H
    D -.-> A
```

## Stack

- HTML5, CSS3, vanilla JavaScript
- Hosting: GitHub Pages

## Repository layout

```
modelos-de-sites/
├── index.html            # showcase hub
├── DESIGN.md             # design direction (source of truth)
├── <niche>/
│   └── index.html        # one landing per niche (20 in total)
├── spec/                 # specs: niches, landing rules, layout/visual review
├── .nojekyll
└── (no LICENSE)
```

## Prerequisites and installation

None. Just serve the folder statically.

## How to run

```bash
python -m http.server 8080
# go to http://localhost:8080 (hub)
# and /<niche>/ index.html for each model, e.g. /moda-ecommerce/
```

Or open each `index.html` directly in the browser.

## Tests and quality

There are no automated tests or CI in this repository (no `package.json` or workflow confirmed). Visual consistency follows `DESIGN.md` and the reviews documented in `spec/revisao-layout.md` and `spec/revisao-visual.md`.

## Technical decisions and trade-offs

- **One self-contained landing per folder**: each model can be served/personalized in isolation and is a ready handoff for the client.
- **Simple hub + 20 static pages**: lightweight, indexable and easy to publish on GitHub Pages.
- **Landing rules documented in `spec/`**: section format and patterns are a norm, not a preference.

## Known limitations and roadmap

- The landings are static (no CMS/backend); content is edited in the HTML.
- No capture-form integration beyond the model itself.

## Development process

An individual project by Kelvin Oliveira, built with orchestrated AI agents and reviewed by the author. The design system, the specs and the review are the author's.

## License and author

This repository has **no license file** (no `LICENSE`). Copyright (c) Kelvin Rebelo de Oliveira.

**Author**: [Kelvin Oliveira](https://github.com/KelvinOliveiraCode) · [Portfolio](https://kelvinoliveiracode.github.io/portfolio/)
