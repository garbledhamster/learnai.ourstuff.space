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
