# Beat News

Personal news site for Zakk Fleischmann's research beats, maintained by Grok Bot (Beat Reporter).
Every item links to its original public source and opens in a new tab.

## How it works

- `_data/beats.json` — the 8 beats (id, name, menu label, color, schedule).
- `_data/items.json` — every item ever posted (`items`) plus per-issue summaries (`issues`), newest first.
  It is generated: the source of truth lives on the Grok Bot box at `/home/box/beat-news/data/items.json`
  and is copied here by `/home/box/beat-news/publish_run.py`. Don't hand-edit it here.
- `index.html` — latest items across all beats (last 7 posting days) plus a color strip of beats.
- `beats/<id>/index.html` — one page per beat (layout `beat`), full history grouped by date.
- `_layouts/`, `_includes/`, `assets/site.css` — templates and styles. No plugins, so GitHub Pages builds it as-is.

## Beat colors

| Beat | Color |
| --- | --- |
| Grok Bot and Agent Assistants | `#2563EB` blue |
| AI Enablement at Large Companies | `#0D9488` teal |
| Agents | `#7C3AED` violet |
| Swarms | `#EA580C` orange |
| Formal Verification, Completeness, and Assurance | `#15803D` green |
| AI-Assisted Engineering, Evals, and Cost | `#A16207` amber |
| Agentic Engineering | `#DB2777` pink |
| AI Security Research (defensive) | `#B91C1C` red |

## Theme credit

Layout ideas (masthead, top menu bar, masonry columns) are adapted from
[The Interesting Times](https://github.com/ohduran/the-interesting-times) Jekyll theme by Álvaro Duran,
released under the MIT license. See `LICENSE-THEME.md`. The styling was rewritten to be minimal, with one solid color per beat.

## Local build

```sh
jekyll build   # Jekyll 3.10, no plugins
```
