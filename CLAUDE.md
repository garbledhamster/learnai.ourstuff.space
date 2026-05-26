# CLAUDE.md

## Purpose

Track durable project context for future agent work in this repo. Keep this file under 500 lines.

## Rules

- Keep entries short, current, and actionable.
- Record only goal, decisions, files changed, verification, risks, and next action.
- Prefer existing project patterns before adding new structure.
- Do not store secrets, API keys, personal data, or temporary chatter here.
- Remove or compact stale notes before this file approaches 500 lines.

## Current Project Shape

- Single-page app driven mainly by `index.html`.
- Learning content lives in `content.yaml`.
- Visual themes live in `themes.yaml`.
- Static assets include `manifest.webmanifest`, `app-icon.svg`, and vendored `vendor/js-yaml.min.js`.

## Change Log

### 2026-05-26

Goal: Add a certification exam tracker dashboard to the Certs path.

Decisions:
- Keep cert blueprint data curated in `content.yaml`.
- Add `certExams` and `certTerms` as the v1 data model.
- Render the dashboard only for Certs topics with `certExam`.
- Persist objective progress in `aiNavigatorCertProgressV1`.

Files changed:
- `content.yaml`
- `index.html`
- `CLAUDE.md`

Verification:
- YAML parsed with vendored `js-yaml`; 7 cert topics resolve to 7 cert dashboards, with no missing term/resource IDs.
- Browser smoke test at `http://127.0.0.1:5188/index.html` showed all Certs dashboards, objective progress persistence, local term panel, mobile no-overflow check, and trainer cert context label.

Risks:
- Official exam blueprints can change; refresh `lastReviewed` and source links before major content updates.

Next action:
- Recheck the dashboard after any cert data update.

### 2026-05-23

Goal: Add a SecAI+ certification section to the existing Certs path.

Decisions:
- Keep Certs content YAML-driven.
- Add CompTIA SecAI+ as one topic in the existing `cert` path.
- Use the official CompTIA certification page as the source URL.

Files changed:
- `content.yaml`
- `CLAUDE.md`

Verification:
- YAML parsed with `vendor/js-yaml.min.js`; Certs path includes 7 topics and resolves `CompTIA SecAI+` to the official CompTIA URL.
- Browser smoke test at `http://127.0.0.1:5188/index.html` showed `CompTIA SecAI+` in the Certs drawer and opened the topic successfully.

Risks:
- SecAI+ details may change over time; refresh against CompTIA before major copy updates.

Next action:
- Verify YAML parses and the Certs path renders with the new topic.
