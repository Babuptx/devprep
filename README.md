# DevPrep / Prep Pro — 700 interview practice questions

**v3.0 (2026-11-05):** Adds 500 original, scenario-based interview practice Q&As across the existing 16 knowledge areas, for 700 total. Five collapsible navigation groups and all original 200 questions remain intact.

- Q&A data remains split across 16 JSON topic files and fetched only on selection.
- The topic sidebar displays actual question counts; local topic search filters the selected subject without downloading other categories.
- Each new item includes an interview-style question, direct baseline answer, deeper explanation, takeaway, topical tags and provenance.
- Original practice synthesis is informed by public 2025–26 interview accounts and engineering references, **not** a claim that questions were personally asked by specific employers or ranked by measured frequency.
- See `research/SOURCES.md` for research provenance and caveats.
- No backend, API credentials or personal candidate records are required.

## GitHub Pages

Repo: https://github.com/Babuptx/devprep  
Site: https://babuptx.github.io/devprep/

Deploy `main` / `(root)` via Settings → Pages. Use an HTTP server when previewing locally (fetching topic JSON from `file://` is restricted in browsers).

## Repository structure

`index.html` contains the lightweight UI and navigation logic; `data/manifest.json` contains all categories and counts; 16 `data/*.json` files contain question records; `research/SOURCES.md` explains research sourcing.

## Future scope

The requested separate section for **coding prompts with algorithmic hints or pseudocode rather than complete solutions** is intentionally deferred to the next release. Do not blend its format into these 500 conceptual and scenario questions.

## Content and rights

Questions are original study prompts; public community reports are inspiration, not verified private interview records. Reuse only with suitable attribution of cited sources and without copying proprietary question banks.
