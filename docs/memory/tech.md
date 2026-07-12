# Tech memory — axantiq (ax-website)

Project-specific stack facts + gotchas. One bullet per fact, dated. No secrets — op:// pointers only.

## Stack
- [2026-07-12] Single static `index.html` (no framework, no build step, no `package.json`) — inline `<style>` and `<script>` only. Font: Google Fonts "Geist Mono" (external `<link>`, not bundled).
- [2026-07-12] Purpose (from `<title>`/`<meta description>` in `index.html` and the GitHub repo description): "aXantiq — AI. Built. Shipped." teaser/gate landing page, ahead of the full site.

## Environment
- [2026-07-12] Deploy target: Vercel. Local checkout is linked (`.vercel/project.json`, gitignored) to Vercel project `ax-website`, org id `team_8EhgMUhGAsuSTXh7ZEaFrsQS`. No `vercel.json` in the repo — default static-site behavior.
- [2026-07-12] No env vars, no server code, no CI config found in the repo.

## Data
- No database. No backend. Fully static.

## Third-party quirks
- [2026-07-12] Outbound contact is a client-side `mailto:` assembled from `["axantiq", "com"].join(".")` behind a mini-gate (type "hello" to reveal) — see `decisions.md` for rationale.
