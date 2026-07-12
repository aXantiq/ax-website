# Decisions — axantiq (ax-website)

ADR-lite. Newest at top. One entry per decision + rationale; ref: ticket/session.

## [2026-07-12] Seed project-memory stack
Adopted the aXantiq project-memory template (`docs/memory/{state,tech,decisions,playbooks}.md`) in this repo, seeded from ground truth (CLAUDE.md/README/git log/`.vercel/project.json` — this repo has no `package.json`). Rationale: memory becomes git-versioned and repo-local instead of laptop-only `~/.claude` notes. Ref: template `ax/tech/dev/02-templates/project-memory` (Drive), session 2026-07-12.

## [2026-07-12] CTA mailto assembled client-side behind a mini-gate
The "Let's build something" CTA does not put an email address in markup; it reveals an inline prompt requiring the visitor to type "hello", then assembles `mailto:` from `["axantiq", "com"].join(".")` and opens it. Rationale (from commit `9c38a5e` "Anti-spam: click-to-reveal mini-gate before mailto opens"): keep the address out of scraped/rendered markup. Ref: `index.html` script block; commit `9c38a5e`.

## [2026-07-12] Password-gated landing page ("swordfish")
The site's first screen is a password gate (password `swordfish`, hinted via a link to the Wikipedia page for the film *Swordfish*) before revealing the services list and CTA. Ref: `index.html` (`#gateScreen`/`#successScreen`); commit `9a557f3` "Initial commit: aXantiq landing page".
