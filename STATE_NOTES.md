# Profile Task State Notes (Aug 18, 2026)

## Repo
- Profile repo: ~/profile (clone of sphangcho203-afk/sphangcho203-afk), branch main, pushed to GitHub.
- Git user configured; commit + push works via shell.

## Palette (soft burgundy)
- charcoal plum #211B24, muted burgundy #8B3A46, dusty rose #B65C65, rainy blue-gray #65758B, warm amber #CB9A6B.

## Live README structure (verified from raw)
- Banner (16:9), anime-girl.png (340px, hero), name/username, italic tagline "building little things inside a big, slightly messy digital world."
- 3 mood badges (flat-square, labelColor=211b24)
- soft-divider (cropped, 100%)
- hi welcome in / small conversation / how to talk to me
- "where else I spend time" — 4 social badges (Telegram t.me/Zulurux98, X x.com/PhangchoSo60056, Spotify open.spotify.com/user/31snn46vcywdzfq3aalcghwr3uru, Instagram instagram.com/nerfed_irl._) as img.shields.io badges with real platform logos, height=26, background 211b24, logoColor 8b3a46.
- palette swatches, things on desk table, project table (7 projects), tool badges (8, custom colors per logo), stats cards (github-profile-summary-cards theme=github_dark, h190), ghchart 8b3a46, currently list, closing divider + thanks note.

## Other files
- REPOSITORY_README_TEMPLATE.md (soft burgundy version)
- .github/workflows/soft-burgundy-check-in.yml
- .github/ISSUE_TEMPLATE: 01-something-feels-off, 02-new-idea, 03-thinking-corner, 04-soft-project-note, config.yml
- assets: soft-banner.png (16:9), anime-girl.png (replaces soft-hero in README), soft-divider.png (cropped), soft-hero.png (still in repo)

## Account
- Name: Songja Phangcho (live)
- Bio: "making things, learning things, leaving a little mess behind." (live)
- Account bio REST PATCH blocked for connectors (403) but was set earlier.

## Pins status
- Only 2 pinned live: nexus-forge, recharza-platform. pinItems mutation NOT exposed to fine-grained PAT (GitHub hides it). Must be manual.
- Repo descriptions applied (6): nexus-forge, ECHO, JarvisApp, recharza-platform, nova-command, ign-api.

## Current task
- Verify social badge layout is clean/aligned in live README. Badges use flat-square style, height=26, same colors — likely fine. Local README file at /home/ubuntu/profile/README.md.

## gh api notes
- gh graphql queries work; mutations like pinItems undefined for this token.
- gh api graphql -F query='...' works for queries; curl POST works for everything.
