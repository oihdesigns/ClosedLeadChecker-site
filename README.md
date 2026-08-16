# ClosedLeadChecker-site — redirect only

This repository exists for one reason: to keep the **old** Blinky Hawk site URL working.

The site moved from `oihdesigns.github.io/ClosedLeadChecker-site` to
**`oihdesigns.github.io/BlinkyHawk`**. Renaming a repository does *not* redirect its GitHub Pages
project URL — GitHub redirects everything about a renamed repo *except* the Pages address — so the
old address would simply 404. This repo takes over the old name and bounces visitors to the new
site instead.

**There is no content here. Do not edit these pages as if they were the site.**
The real site lives in the [BlinkyHawk](https://github.com/oihdesigns/BlinkyHawk) repository.

## What is in here

| File | Redirects to |
|---|---|
| `index.html` | `BlinkyHawk/` |
| `user-guide.html` | `BlinkyHawk/user-guide.html` |
| `firmware-manual.html` | `BlinkyHawk/firmware-manual.html` |
| `quick-start.html` | `BlinkyHawk/quick-start.html` |
| `404.html` | `BlinkyHawk/` — catches every other old path |

Each page redirects three ways so it works regardless of the visitor's browser or settings: a
`<meta http-equiv="refresh">`, a `location.replace()` script, and a visible link to click if
neither fires. Each also carries a `<link rel="canonical">` pointing at the new page, so search
engines transfer ranking to the new address rather than treating it as a duplicate.

## Setup

Pages must be configured to deploy from GitHub Actions:
**Settings → Pages → Build and deployment → Source: GitHub Actions**.
The workflow in `.github/workflows/deploy-pages.yml` then publishes on every push to `main`.

## Retiring this

Keep it as long as the old URL might still be in circulation — printed inserts, bookmarks, forum
posts, search results. It costs nothing to leave in place.
