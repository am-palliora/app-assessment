# app-assessment

Independent usability/quality assessments of Palliora-ecosystem apps.
Each app gets its own top-level folder; each kind of assessment gets its
own subfolder within that. This repo is the ongoing home for all future
assessments like this one -- a new app being reviewed means a new
top-level folder, not a new repo.

## Structure

```
<app-name>/
  usability/
    report.md        -- findings, priority-rated (High/Medium/Low), with a Wow Factor section
    screenshots/      -- one baseline (clean) shot plus numbered, annotated shots -- each
                         annotated shot has a colored box + numbered badge drawn directly
                         onto the real rendered page, matching a numbered finding in report.md
```

Future assessment types (performance, accessibility, security, etc.) would get their own
sibling subfolder under the same app, e.g. `<app-name>/performance/`, `<app-name>/accessibility/`
-- `usability` is just the first one.

## Current contents

| App | Assessment | Status |
|---|---|---|
| [explorer](explorer/usability/report.md) | Usability (Manas testnet explorer, https://manas.palliora.org) | Complete -- 2026-10-13 |

## Methodology notes (apply across all assessments in this repo)

- Findings are grounded in the real, live app at the time of review (real screenshots,
  real clicks, real DOM inspection) -- not assumptions about how it's probably built.
- Annotated screenshots mark issues directly on the actual rendered UI (a colored box +
  numbered badge drawn into the live page before capture), not freehand markup on a static
  image after the fact -- the box is pixel-accurate to the real element.
- Priority is assigned per finding: **High** (breaks trust or a core flow -- dead links,
  contradictory data, broken navigation), **Medium** (confusing or unpolished but has a
  workaround), **Low** (cosmetic or minor).
- A **Wow Factor** section is included where the goal is explicitly first-impression /
  outside-visitor appeal, not just "does it work" -- what would make someone unfamiliar
  with Palliora actually get excited, separate from the bug list.
