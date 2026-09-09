# ENGINEER WORLD // VISUAL SYSTEM

This profile uses one deliberate visual language: **retro 16-bit engineering UI fused with futuristic HUD instrumentation**. The visual layer can be cinematic; the technical claims underneath must stay concrete, selectable, and inspectable.

---

## 01 / DESIGN INTENT

**Tone:** pixel-engineer mainframe, advanced workshop, governed runtime, retro arcade instrumentation.

The system should feel:

- authored rather than templated;
- technical without becoming sterile;
- playful without becoming childish;
- cinematic without burying the engineering;
- dense with information, not decorative noise;
- consistent from hero to footer.

It should not become:

- a generic neon badge wall;
- random cyberpunk cards with no hierarchy;
- a wallpaper followed by unrelated Markdown;
- an imitation of a film UI frame-for-frame;
- a personal social-media landing page.

---

## 02 / CORE PALETTE

| Token | Value | Role |
|---|---|---|
| `OBSIDIAN` | `#0D1117` | primary background |
| `REACTOR_CYAN` | `#00F0FF` | primary signal / structure |
| `TITANIUM_GOLD` | `#FFD700` | active engineering accent |
| `STARK_CRIMSON` | `#E63946` | warning / execution accent |
| `ICE_TEXT` | `#EAFBFF` | primary light text |
| `STEEL_BLUE` | `#16394B` | low-priority grid / structure |

The palette should stay controlled. Cyan owns the interface. Gold marks active capability. Crimson marks execution or warning. Obsidian keeps the profile grounded.

---

## 03 / PIXEL RULES

1. Use crisp geometric edges and explicit grid alignment.
2. Avoid soft anti-aliased ornament when a hard pixel edge works.
3. Use glow as a signal hierarchy tool, not as fog.
4. Keep micro-HUD text short and decorative; long explanations belong in Markdown.
5. Symmetry is useful for system status and divider assets; project content can break symmetry when information requires it.

SVG assets use `shape-rendering="crispEdges"` where possible so the system stays sharp at GitHub display sizes.

---

## 04 / TYPOGRAPHIC ROLES

### DISPLAY

Used for the hero and major system labels.

- uppercase;
- short phrases;
- wide spacing;
- high contrast.

### TERMINAL

Used for runtime state, labels, status codes, and technical metadata.

Preferred fallback:

```text
monospace / ui-monospace / SFMono-Regular / Menlo / Consolas
```

### DOCUMENT

Native GitHub Markdown remains the primary layer for long-form technical explanation. The profile should still make sense if decorative imagery fails to load.

---

## 05 / VISUAL GRAMMAR

### REACTOR

The reactor symbol represents the active system core: energy, orchestration, and runtime state.

### FRAME

Mechanical HUD frames represent a bounded capability or project surface.

### GRID

Grids imply measurable structure, diagrams, and execution space. They should never overpower the actual content.

### SIGNAL COLORS

- cyan = available / informational
- gold = active / important
- crimson = execution / warning
- white = primary readable text

### DIVIDERS

Section dividers create rhythm between major modules. They should be thin enough to separate sections without becoming another hero banner.

---

## 06 / ASSET MAP

| Asset | Role |
|---|---|
| `assets/engineer-world-hero.svg` | main identity / workshop mainframe |
| `assets/engineer-divider.svg` | section rhythm / reactor link |
| `assets/engineer-project-frame.svg` | project showcase / blueprint surface |
| `assets/engineer-stack.svg` | technology module inventory |
| `assets/engineer-footer.svg` | closing system-status transmission |

Older assets may remain as design history, but the files above define the active profile system.

---

## 07 / README HIERARCHY

```text
ENGINEER WORLD HERO
        ↓
MAIN_FRAME / DIRECTIVE
        ↓
ACTIVE SYSTEMS
        ↓
TECH MODULES
        ↓
SYSTEM BLUEPRINT
        ↓
ENGINEERING PROTOCOL
        ↓
ARCHIVE / TRANSMISSION
```

The descent is intentional: atmosphere first, then proof.

---

## 08 / CONTENT RULES

1. Major visuals must support a real informational role.
2. Technical claims must remain selectable Markdown, not image-only text.
3. Public and private systems must be classified accurately.
4. Private systems may be described architecturally without exposing secrets or private source.
5. Project descriptions should state the actual engineering problem, not marketing language.
6. Status labels such as `ACTIVE`, `ALPHA`, `LAB`, and `SEALED` must stay truthful.
7. The profile must avoid personal-identifying information unrelated to the engineering work.
8. A decorative UI element should be removed if it weakens hierarchy or readability.

---

## 09 / WRITING VOICE

Preferred:

> A deterministic local action kernel handles known device operations before cloud reasoning.

Avoid:

> Revolutionary next-generation AI experience powered by cutting-edge innovation.

The visual system can be dramatic. The writing should remain precise.

---

## 10 / FINAL RULE

**The interface earns attention. The architecture earns trust. The evidence earns the ship.**
