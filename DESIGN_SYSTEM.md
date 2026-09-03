# CIVILIZATION ZERO // VISUAL SYSTEM

This repository uses a deliberate visual language instead of a collection of unrelated banners. The goal is to make technical content feel like one coherent archive while remaining readable inside GitHub's Markdown renderer.

---

## 01 / DESIGN INTENT

**Tone:** classified engineering archive, celestial infrastructure, restrained anime-civilization influence.

The system should feel:

- authored rather than templated;
- technical without becoming sterile;
- cinematic without burying the information;
- dense without becoming noisy;
- dark without collapsing into pure black;
- ornamental only where ornament reinforces hierarchy.

It should not feel like:

- a generic neon developer profile;
- a badge wall;
- a cyberpunk dashboard assembled from random cards;
- a wallpaper with text underneath;
- a personal social-media landing page.

---

## 02 / COLOR LANGUAGE

| Token | Intent | Approximate value |
|---|---|---|
| `VOID` | deepest background | `#070A10` |
| `OBSIDIAN` | secondary surface | `#101725` |
| `ASH` | quiet structural surface | `#181D28` |
| `IVORY` | primary warm text / line | `#F2E4D0` |
| `BONE` | subdued text | `#B8B5C0` |
| `DUSK` | muted violet structural accent | `#6D5A78` |
| `EMBER` | warm signal highlight | `#F0D8B8` |

The palette avoids saturated purple as a dominant brand color. Violet appears only as atmospheric depth.

---

## 03 / TYPOGRAPHIC ROLES

GitHub-hosted SVGs cannot rely on external web fonts, so the visual system uses strong role separation rather than fragile font dependencies.

### DISPLAY

Used for archive titles and large system names.

- uppercase;
- wide tracking;
- high contrast;
- short phrases only.

### TERMINAL

Used for metadata, coordinates, release labels, and system states.

Preferred stack:

```text
ui-monospace, SFMono-Regular, Menlo, Consolas, monospace
```

### DOCUMENT

Native GitHub Markdown typography is deliberately kept for long technical explanation. This prevents the profile from becoming an unreadable poster.

---

## 04 / VISUAL GRAMMAR

### Frames

Large modules use restrained rounded frames with low-opacity warm strokes.

```text
┌──────────────────────────────────────────────┐
│  metadata                                    │
│                                              │
│  primary information                        │
│                                              │
│                                  signal      │
└──────────────────────────────────────────────┘
```

### Rings

Celestial rings represent control, coordination, or a system boundary. They are structural symbols, not decoration pasted everywhere.

### Lines

Directional lines should imply one of three meanings:

- data/control flow;
- hierarchy;
- measured alignment.

### Signal points

Small warm dots indicate an active or observed system state.

### Ruins / skyline

The civilization imagery belongs primarily in the hero and major archive surfaces. Technical modules should become progressively more diagrammatic as the reader moves down the page.

---

## 05 / CONTENT HIERARCHY

The profile follows a deliberate descent from atmosphere into proof.

```text
CINEMATIC IDENTITY
      ↓
OPERATOR CONSOLE
      ↓
PROJECT DOSSIERS
      ↓
SYSTEM BLUEPRINT
      ↓
CAPABILITY MATRIX
      ↓
ENGINEERING PROTOCOL
      ↓
DEEP ARCHIVE DOCUMENTATION
```

This keeps the opening memorable while ensuring the lower half rewards technical inspection.

---

## 06 / ASSET MAP

| Asset | Role |
|---|---|
| `assets/civilization-hero.svg` | primary cinematic identity |
| `assets/civilization-console.svg` | operating-state overview |
| `assets/civilization-archives.svg` | selected-system visual index |
| `assets/civilization-blueprint.svg` | cross-project architecture diagram |
| `assets/civilization-footer.svg` | closing transmission / visual endpoint |

Older experimental assets may remain in the repository as design history, but the files above form the current profile system.

---

## 07 / README COMPOSITION RULES

1. **Never stack large images without real text between them.**
2. **Every visual module needs an informational purpose.**
3. **Technical claims belong in selectable Markdown text, not only inside images.**
4. **Tables are used for comparison, not as generic card containers everywhere.**
5. **Badges are secondary metadata, never the visual identity.**
6. **The lower the reader goes, the more specific the content should become.**
7. **Decorative language must not obscure actual project status.**
8. **Private systems may be described at architecture level without exposing private source or operational secrets.**

---

## 08 / WRITING VOICE

Preferred:

> A deterministic local action kernel handles known device operations before cloud reasoning.

Avoid:

> Revolutionary AI-powered next-generation super assistant experience.

Preferred writing is concrete, architectural, and testable. The visual world can be dramatic; the engineering claims should remain ordinary and inspectable.

---

## 09 / POLISH CHECKLIST

Before changing the profile, verify:

- [ ] the hero still has a clear focal point;
- [ ] there is no giant dead zone between modules;
- [ ] repeated card patterns have not taken over the page;
- [ ] long text remains native/selectable Markdown;
- [ ] every project description contains a real engineering problem;
- [ ] architecture diagrams reflect the written model;
- [ ] status labels are truthful;
- [ ] links point only to intentionally public surfaces;
- [ ] the page works even if decorative imagery fails to load;
- [ ] new visuals match the existing frame, spacing, and signal language.

---

## 10 / FINAL RULE

**Atmosphere earns attention. Specificity earns trust.**

The repository should always contain both.
