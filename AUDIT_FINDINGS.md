# Live profile audit — 2026-08-18

## Issues spotted in live render (desktop, light mode)

1. **Hero GIF too small vs heading width**: name heading (620px) is much wider than the 250px GIF; the composition feels top-heavy with a thin GIF centered above a wide heading. → Make GIF slightly bigger (300px) and heading proportionally tuned (maybe 560), or keep; consider GIF width 300.
2. **Divider renders as dark/black band**: soft-divider.png width=100% stretches the 2688x245 dark image across full page width — it looks like a black bar. It's intentional dark, but it reads as a huge dark band. Could soften: reduce width (e.g., 70%) so it reads as a decorative brush stroke, not a full-width bar.
3. **"hi, welcome in" heading at 360px** is much narrower than the 100%-width divider above it — hierarchy inconsistent. Also heading image sits inside `##` which adds a visible anchor line under it; the anchor icon + line under an image heading looks odd.
4. **Name heading image inside `<h1>`**: GitHub wraps it in a link + shows anchor icon next to it — ugly but unavoidable. Could reduce by removing h1 and just using a centered img (like hero GIF). Actually h1 is useful for semantics; keep but note.
5. **Mood badges fine**, social badges fine.
6. **Overall spacing**: large gaps from `<br/>` look fine.
7. **Bio in profile header** (sidebar): "making things, learning things, leaving a little mess behind." — matches vibe.
8. Activity cards: summary-cards theme github_dark — dark cards on light page look consistent with the aesthetic; fine.
9. Pinned repos: user confirmed done — 6 pinned show correctly.

## Improvement plan
- Hero GIF: 250 → 300px.
- Name heading image: 620 → 540px (scales better).
- Welcome heading image: 360 → 400px.
- Dividers: width 100% → 68%, centered, so they read as soft brush strokes (not black bars).
- Keep everything else.
