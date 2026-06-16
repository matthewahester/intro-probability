# intro-probability

Public-facing Quarto **course-materials site** for an undergraduate
**Introduction to Probability** course, assembled by Matt Hester.
Sibling to the main site [matthewhester.com](https://matthewhester.com);
intended to live at `/intro-probability/` under that domain.

This is **assembled undergraduate course material** — synthesized lesson
notes, hands-on R/Quarto simulation labs, and curated references. It is a
durable public resource site, **not** a record of a currently scheduled
section, and **not** an LMS.

## Status

Assembled from a course-material build (2026-06). Topic flow, notes,
labs, and resources are in place. Dates, weights, and final policies are
not sealed and are authoritative in the LMS whenever the course runs.
Treat the site as a coherent draft, not a final release.

## What this site holds

- **Notes** — the weekly instructional spine (15 weeks, five parts):
  uncertainty and probability models, sample spaces and rules,
  conditional probability and independence, Bayes' rule, counting,
  discrete and continuous random variables, expectation and variance,
  the standard distributions, joint behavior, and limit theorems.
- **Labs** — four reproducible R + Quarto simulation labs (Monte Carlo
  basics, Bayes by simulation, simulating discrete models, the law of
  large numbers and the central limit theorem).
- **Resources** — a notation glossary, a one-page distribution
  reference, and R/Quarto setup instructions.

The primary spine is *Introduction to Probability* by Grinstead and Snell
(GNU FDL), supplemented by MIT OpenCourseWare 18.05 (CC BY-NC-SA 4.0).
These notes are the course's **own synthesis**, attributed at the
section level — not bulk-copied source text. All examples use synthetic
data with seeds set.

## What does not go in this repo

Anything private to a graded offering: answer keys, assessment items,
rubrics, point values, due dates, student data, or any directory from
the private course build (`_state/`, `assessment_shadow/`,
`source_text/`, `run_reports/`, `accessibility/`). See
[`CLAUDE.md`](CLAUDE.md) for the full list. The operational, graded side
of any live offering lives in **Blackboard (the LMS)**, which is
authoritative.

## Local development

```bash
quarto render     # build to _site/
quarto preview    # live preview
```

The weekly notes and labs contain executable `{r}` chunks (figures), so
a full render needs **R + knitr** installed. To validate structure,
links, and images without R:

```bash
quarto render --no-execute   # renders prose + code, skips R execution
```

## Layout

```
intro-probability/
├── _quarto.yml              # site config, navbar, sidebar, render allow-list
├── index.qmd                # landing page (hero + overview)
├── syllabus.qmd             # public course overview
├── schedule.qmd             # week-by-week topic map
├── notes/                   # weekly instructional notes + index
├── labs/                    # reproducible R/Quarto simulation labs + index
├── resources/               # glossary, distribution reference, setup + index
├── assets/                  # hero.png + icon.png (course identity art)
├── styles.css               # course-family palette
├── CLAUDE.md                # privacy + editing rules
└── README.md                # this file
```

No CI and no deploy pipeline in this repo. The combined site is
assembled and deployed by the hub repo (`matthewhester-site`). Local
builds only here; commits are deliberate and user-driven.
