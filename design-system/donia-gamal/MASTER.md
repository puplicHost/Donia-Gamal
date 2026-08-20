# Donia Gamal — "The Campaign Ledger" / MASTER

Source of truth for the Donia Gamal portfolio design system (single-file `index.html`).
This master file is the root; page-specific overrides belong in `pages/`.

## Concept

The page behaves like a well-kept agency production book. In a hiring manager's world —
briefs, production pipelines, QC stamps, deliverables, timeline rows — those artifacts
become the visual language. One signature element (the Q.C. rubber stamp + self-filling
numbered pipeline) carries the boldness; everything else stays disciplined.

## Palette (semantic aliases → primitives)

| Token | Value (primitive) | Role |
|---|---|---|
| `--color-ink` | `#131A18` | deep spruce ink — text, dark sections |
| `--color-ink-soft` / `--color-ink-deep` | `#1E2825` / `#0D1210` | hover / footer shades |
| `--bg` | `#F2EFE6` | ledger paper — page ground |
| `--bg-surface` | `#FFFDF7` | digital linen — cards, briefs |
| `--bg-mist` | `#E7E3D6` | hover wash, meta bars |
| `--color-accent` | `#E8A33D` | saffron — single loud accent (decorative/non-text only on light surfaces) |
| `--color-accent-deep` | `#B46F10` | stamp saffron — pass 3:1 on linen for UI, icons, large text |
| `--color-text-muted` / `--color-text-faint` | `#616B65` / `#A9AFA8` | secondary / faint text |
| `--color-line` etc. | `rgba(19 26 24 / .14…)` | hairlines from ink channels |

## Typography

| Role | Face | Usage |
|---|---|---|
| Display | El Messiri 600/700 | Arabic headings, numbers, monogram |
| Latin display | Archivo 800/900 | logotype, brief fields, stat values |
| Body | IBM Plex Sans Arabic 400–700 | Arabic UI, paragraphs, labels |
| Utility | JetBrains Mono 500/600 | every date, period, kicker, EN tag — record labels |

Scale: 72px H1 hero → 46px section → 26px card titles → 16px body → 0.6–0.8rem mono labels.
All English label text is uppercased mono with 0.1–0.2em tracking.

## Layout rules

- `--container: 1220px`; sections padded `clamp(84px, 10vw, 130px)`.
- Spacing scale: 4px base unit (`--space-1…--space-16`); component paddings/gaps align to it.
- Everything aligns to hairline-ledger grid; section kicker = mono label + 220px rule.
- Layout devices: ledger stats strip, account brief card, service ledger rows (3-col),
  résumé rows (mono period + saffron dot spine), testimonial quote cards.
- Starting in RTL: all inset offsets use logical properties.

## Components

- **Buttons**: 1.5px ink border, `--r-sm`, hard offset shadow `4px 4px 0`; hover presses
  2px in (shadow collapses). Variants: dark (ink), saffron (accent), ghost.
- **Cards**: linen surface, hairline border, `--r-lg`; hover `translateY(-6px)` + hard-shadow.
- **Images**: sharp corners (0 radius) inside bordered frames — never rounded.
- **Pipeline phases**: numbered 01–06 (genuine sequence), self-fill on scroll with
  per-phase 140ms stagger; phase ticks flip saffron in sequence.
- **Q.C. stamp**: SVG text ring "Q.C. APPROVED · DONIA GAMAL", multiply blend,
  stamp-down keyframe at load, only element with rotation boldness.

## Motion

- `--ease: cubic-bezier(.22,1,.36,1)`; reveals 0.8s (opacity+28px rise), stagger via `--rd`.
- Hover micro-interactions 180–400ms. `prefers-reduced-motion` disables all motion and
  renders final states (stamp static, reveals visible, scroll auto).

## Accessibility floor

- `:focus-visible` 2px saffron outline, offset 3px (3:1 contrast vs surfaces).
- Contrast policy: small text on light surfaces uses ink/ink-soft/sage (≥4.5:1); small text on
  dark surfaces uses saffron/sage-light/pale (≥7:1); saffron-deep is reserved for icons,
  borders, backgrounds, and large text (≥3:1). Stars, kickers, tags never drop below AA.
- Modals: focus moves to close button on open, restored on close, Tab trapped inside,
  Esc closes, body scroll locked, backdrop click closes, `overscroll-behavior: contain`.
- Clickable cards are keyboard operable (Enter), `cursor: pointer`, hover never the
  only affordance. Form uses visible above-field labels, inline success status.
- Buttons have `:active` press states; hero entrance uses a 6-step orchestrated rise-in
  (80–400ms stagger) that is disabled entirely under reduced motion.

## Breakpoints

- `≤1100px`: hero stacks, pipeline 3-col, services 2-col, about stacks.
- `≤991px`: work 1-col, résumé rows stack, contact stacks.
- `≤768px`: mobile nav panel, buttons full width, pipeline single column, modal 1-col.
- `≤480px`: hard shadows shrink to `--shadow-hard-sm`, type scale compresses.

## Anti-patterns (do not reintroduce)

- No gradients except the single reel-caption shade and the identity-panel top rule
  (both tokenized); no glassmorphism; no emoji icons; no arbitrary numbering (only the
  pipeline sequence is numbered); no raw hex/rgba in component rules.