---
name: sync-resume
description: Sync the GitHub profile README at ./README.md from the master resume doc at ../resume-projects.md. Refreshes the blurbs of the curated featured projects and proposes additions/removals to the skillicons rows when the resume's tech footprint shifts. Use when the user says "update my profile", "sync the profile readme", "/sync-resume", or asks to refresh this repo's README from the resume.
---

# sync-resume (mqmalagris)

This is the GitHub profile repo (`github.com/mqmalagris/mqmalagris`). Its `README.md` renders on the user's profile page. The skill keeps that file in step with the master resume doc.

## Constants

- **Resume file (always this path):** `C:/Users/malag/projects/side/resume-projects.md`
- **Target file:** `./README.md` at this repo's root
- **GitHub username:** `mqmalagris`

If the resume file is missing, stop and ask. Never write to a different resume path.

## What this skill is and isn't

The profile README is **curated**, not exhaustive. The user hand-picks which side projects appear (currently yield-curves, CalculeOnline, Ephemask). The resume doc lists everything, including work the user does not want surfaced on a public profile.

Therefore:

- **Refresh** existing featured-project blurbs from their resume sections.
- **Refresh** the intro/about copy only if the user explicitly asks.
- **Do not auto-add** new featured projects when they appear in the resume. Surface them as candidates and let the user decide.
- **Do not auto-remove** featured projects when they're missing from the resume — flag and ask.
- **Preserve** hand-edited fields: contact email, project order, public live-URL links the user has added (e.g. `https://ephemask.com/`), the Background paragraph.

## Args

Optional free-form list of project names to scope the update (e.g. `/sync-resume yield-curves calculeonline`). Match leniently against the resume's display names. If no args, refresh every project currently featured in the README.

## Flow

### 1. Read both sides

Run in parallel:

- Read `./README.md` in full.
- Read `C:/Users/malag/projects/side/resume-projects.md` in full.

Identify the featured-project list from the README (sections under `## Selected projects`).

### 2. Match each featured project to a resume entry

The README uses the same display name as the resume (e.g. `### [yield-curves]…` ↔ `### yield-curves — Rust Yield Curve Library`). Match on the heading text, ignoring trailing descriptors. If a featured project has no resume match, flag it and ask before editing.

### 3. Draft updated blurbs

For each match, prepare a single-paragraph blurb that reflects the resume's current bullets, in the README's voice:

- Lead with the same one-line framing the resume uses.
- Compress the resume bullets into prose, not a bullet list — the README format is paragraph-per-project.
- Keep the same length budget as the existing blurb (±20%). The README is not a re-print of the resume.
- Preserve any live-URL link the user has wired into the heading (`### [Project](https://...)`) — do not strip it.

### 4. Check the skillicons rows

Compare the resume's "Technical Skills Summary" table against the icon rows. Propose adds when the resume lists a tech that has a skillicons identifier and isn't already represented; propose removals only if a row contains a tech the user has clearly dropped from the resume.

**Do not invent skillicons codes.** If unsure whether `skillicons.dev` supports a given tech, fetch `https://skillicons.dev` once to confirm before adding.

Tech that has no skillicons icon (Hono, Axum, LoopBack, Strapi, Capacitor, BigCommerce, Miva, Shopify, ReCharge, Stripe, DocuSign, Turborepo, EAS, Wrangler, Fly.io, Anthropic SDK, OpenAI SDK, Langchain, Playwright as of writing) is intentionally absent — the icons are a vibe, not a complete inventory. Do not "fill the gap" with shields.io badges unless the user asks.

### 5. Propose, then write

Show the user, before editing:

- Per project: the current blurb and the proposed replacement, with a one-line rationale ("resume now lists Svensson 1994 fit and Nelder-Mead optimizer — added").
- Any proposed icon-row changes, also with rationale.
- Any candidate new featured projects ("`mami.care` is in the resume but not the README — surface it?") — present, do not apply.
- Any flagged removals ("`SynthChord` is in the README but no longer in the resume — keep, remove, or rename?").

Wait for explicit confirmation. Then apply with `Edit` (not `Write`) so the diff stays minimal. After writing, confirm the change in one sentence — do not re-print the file.

## Style — match the existing README

- **Project sections:** `### [Name](optional-url) — Short descriptor`
- **Blurb:** one paragraph, prose. Concrete capabilities and architectural choices, no marketing adverbs. If a sentence reads like a recruiter wrote it, rewrite it.
- **No emojis.** Ever.
- **No badges other than skillicons.** Adding shields.io mid-row breaks the visual grouping.
- **Em-dashes (—), not hyphens**, in headings and intro lines, matching the existing copy.

## What NOT to touch

- Contact email — the user maintains this manually.
- Background section (CEFET-RJ line) — static personal info.
- Project order — curation choice.
- Section headings (`## Selected projects`, `## Stack`, `## Background`, `## Contact`) — they're the structural skeleton.
- The `[Arctic Leaf Inc.](https://arcticleaf.io)` link in the intro — the user explicitly chose to call out the employer.

## After-write checks

- Verify all four `##` sections still exist in the file.
- Verify all skillicons URLs still parse as `https://skillicons.dev/icons?i=…`.
- Verify no project's heading lost its live-URL link.
- Report: which blurbs changed, in one sentence.

## Publishing

This skill writes only the local file. After it confirms the edit, remind the user to commit and push:

```
rtk git add README.md
rtk git commit -m "Sync profile README from resume"
rtk git push
```

Do not run `git push` autonomously — pushes are remote actions and require explicit user go-ahead.
