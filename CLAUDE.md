# Instructions for Claude Code — brattlefly/wiki

This repo powers the internal BrattleFly wiki (Docsify, hosted on GitHub Pages).

## Standing rule: review before push

Never run `git push` without first showing a summary of the changes (or `git diff`) and getting explicit confirmation. This applies every time, no exceptions — including small edits.

Workflow for any content change:
1. Make the edit(s) locally.
2. Show a plain-language summary of what changed (which page, what was added/removed/edited) — not just the raw diff.
3. Wait for a go signal ("go," "confirm," "push it," etc.).
4. Commit with a short, descriptive message and push to `main`.

## Other standing rules

- "BrattleFly" is always capitalized with a capital F.
- Trico Unlimited / Battenkill content must stay clearly separated from BrattleFly's own Connecticut River / West River content — never merge or conflate them on a page.
- Specific fishing locations never get added to any page in this repo — location non-disclosure applies internally too, not just on the public site.
- Match the existing plain, direct voice already used across the wiki pages — no marketing gloss, no superlatives.

## Structure

- `_sidebar.md` — nav; update this if a new page gets added
- `README.md` — home page
- One markdown file per section (`entities-legal.md`, `brand-voice.md`, `people.md`, `operations.md`, `marketing-media.md`, `roadmap.md`)
- Site rebuilds automatically via GitHub Pages within a minute or two of a push to `main`
