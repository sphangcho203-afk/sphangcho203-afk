# Social badge investigation findings (Aug 18, 2026)

## Current README section (lines 56-71 of ~/profile/README.md)
- "where else I spend time" section with 4 shields.io badges, height=26:
  - Telegram: `badge/Telegram-211b24?style=flat-square&logo=telegram&logoColor=8b3a46` → link https://t.me/Zulurux98
  - X: `badge/X-211b24?style=flat-square&logo=x&logoColor=8b3a46` → link https://x.com/PhangchoSo60056
  - Spotify: `badge/Spotify-211b24?style=flat-square&logo=spotify&logoColor=8b3a46` → link https://open.spotify.com/user/31snn46vcywdzfq3aalcghwr3uru
  - Instagram: `badge/Instagram-211b24?style=flat-square&logo=instagram&logoColor=8b3a46` → link https://www.instagram.com/nerfed_irl._

## Verified render issues (via rsvg-convert rendering of live shields.io responses)
- badges_fresh.jpg: Telegram, Spotify, Instagram render fine with colored logo + dark label.
- X badge (`logo=x`) has a baked-in defect: the embedded X icon is double-layered
  (a burgundy outline glyph PLUS a white bold "X" text glyph overlapped) — confirmed in
  x_variants.jpg and nologo_crop.jpg. Also when rendered small, the white glyph dominates,
  logo appears faint/broken. Root cause: shields.io embeds simple-icons `x` icon at
  `fill="#8b3a46"` but the SVG viewBox/content draws it twice (logo path + fallback text).
- `logo=twitter` with label="" (empty label via %E2%80%83 space char) renders a tall
  blank-ish badge — avoid.
- `logo=twitter` with label "X" renders oversized white X glyph (logoSize default too big).
- Best fix candidates tested:
  1. `badge/X-211b24?style=flat-square&logo=twitter&logoColor=8b3a46&logoSize=auto` — need render check
  2. `badge/X-211b24?style=flat-square&logo=x&logoColor=8b3a46&logoSize=auto` — still doubled per render
  3. Use custom local SVG icon image instead of shields.io for X.

## Working pattern for the other 3 badges: keep as-is.

## Render toolchain
- sudo apt-get install librsvg2-bin (already installed)
- rsvg-convert -w <px> in.svg -o out.png; Python/PIL for strips.

## README context
- Repo: ~/profile (clone of sphangcho203-afk/sphangcho203-afk), branch main, commit d22c1fe was layout fix, latest push e91cda2 harmonization.
- Palette: charcoal plum #211B24, muted burgundy #8B3A46, dusty rose #B65C65, rainy blue-gray #65758B, warm amber #CB9A6B.
- After edits: git add, commit, git push origin main, then verify live README via
  curl https://raw.githubusercontent.com/sphangcho203-afk/sphangcho203-afk/main/README.md
