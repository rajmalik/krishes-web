# CLAUDE.md

Guidance for Claude Code in this repo.

## What this is

The public Krishes Inc. website (`www.krishes.com`). Static HTML/CSS/JS, no
framework, no build, no package.json. Deployed by Vercel from `main`; other
branches and PRs get preview URLs.

The Meridian app (backend, web app, mobile) lives in a different, private repo
(`rajmalik/proceedings`). Nothing here talks to it; the only outbound links are
Google Fonts and the App Store listing.

## Working on it

- Preview: `npx serve .` → http://localhost:3000. Check every changed page at
  desktop width and at 375 px.
- All colours, fonts and spacing come from `tokens.css`. Add a token there
  rather than hard-coding a value in `styles.css` or the HTML.
- Style: monochrome (black on white), tight spacing, small corners, few boxes,
  no pills.
- Every page repeats the same `<head>`, nav and footer. A change to one of them
  goes into all four pages in the same commit.
- Keep it dependency-free: no npm packages, no bundler, no CDN scripts.

## Repo rules

- This repo is **public**. Never commit secrets, internal docs, personal phone
  numbers or addresses, or anything from the private app repo.
- Commit as `rajmalik` (the repo-local git identity), not a work identity.
- Work on a branch and open a PR; merging to `main` deploys to production.
