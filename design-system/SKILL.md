# Stable Design System

> Version: 1.0
> Owner: Caleb Zimmermann
> Tier: Foundation

The design language for all Stable Company software. Every UI, dashboard, prototype, and customer-facing tool references this system. Override only with explicit justification.

---

## Principles

1. **Typography does the work.** Size, weight, and spacing communicate hierarchy — not color, not icons, not decoration.
2. **Earn every element.** If it doesn't help the user make a decision or take action, remove it.
3. **No emoji. No gradients. No gimmicks.** Use words, not pictographs. Use flat color, not gradients. Let the content be the interface.
4. **Warm, not cold.** Avoid pure whites and blue-grays. Use warm off-whites and stone tones. Software should feel like a workshop, not a hospital.
5. **Quiet confidence.** The UI doesn't need to prove it's smart. Agent intelligence surfaces naturally — through better content, not flashy badges.
6. **Midwest sensibility.** Honest, functional, unpretentious. Would this feel right in a conference room in Columbus? If it feels like it belongs in a San Francisco pitch deck, rethink it.

---

## Color Tokens

### Backgrounds
| Token | Hex | Usage |
|-------|-----|-------|
| `bg-primary` | `#FAFAF7` | Page background. Warm off-white. |
| `bg-surface` | `#FFFFFF` | Card/panel surfaces. |
| `bg-surface-hover` | `#F5F5F0` | Hovered cards and interactive rows. |
| `bg-muted` | `#F0EFEA` | Secondary backgrounds, table headers, input fields. |
| `bg-sunken` | `#E8E6E1` | Inset areas, code blocks, disabled states. |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `text-primary` | `#1A1A1A` | Headings, primary content. Near-black, not pure black. |
| `text-secondary` | `#5C5C5C` | Body text, descriptions. |
| `text-tertiary` | `#8A8A80` | Captions, timestamps, metadata. Warm gray. |
| `text-disabled` | `#B5B5AD` | Disabled text, placeholders. |

### Accent — Sage
| Token | Hex | Usage |
|-------|-----|-------|
| `sage-700` | `#3D6B50` | Primary actions, active nav, links. Dark sage. |
| `sage-600` | `#4E8A65` | Buttons, active states. |
| `sage-500` | `#6BA37E` | Hover states, secondary emphasis. |
| `sage-100` | `#E8F0EB` | Subtle backgrounds for sage-accented elements. |
| `sage-50` | `#F2F7F4` | Very light sage tint for selected rows. |

### Status
| Token | Hex | Usage |
|-------|-----|-------|
| `status-good` | `#3D6B50` | On track, healthy, positive. Uses sage (not green). |
| `status-good-bg` | `#F2F7F4` | Background for good status. |
| `status-warn` | `#A67B3D` | At risk, needs attention. Warm amber/copper. |
| `status-warn-bg` | `#FBF5EC` | Background for warning status. |
| `status-bad` | `#A63D3D` | Off track, critical, failed. Muted red-brown. |
| `status-bad-bg` | `#FBF0F0` | Background for bad status. |
| `status-neutral` | `#8A8A80` | Stable, no change, informational. |

### Borders
| Token | Hex | Usage |
|-------|-----|-------|
| `border-default` | `#E0DED8` | Card borders, dividers. Warm, not cool. |
| `border-subtle` | `#ECEAE4` | Very subtle separators. |
| `border-strong` | `#C5C3BC` | Focused inputs, emphasized dividers. |

---

## Typography

Use the system font stack. No custom fonts needed — the native stack is clean and fast.

```
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif;
```

### Scale
| Name | Size | Weight | Line Height | Usage |
|------|------|--------|-------------|-------|
| `display` | 32px | 700 | 1.1 | Page titles, hero numbers |
| `title` | 20px | 700 | 1.3 | Section headers |
| `heading` | 15px | 600 | 1.4 | Card titles, subsections |
| `body` | 14px | 400 | 1.6 | Primary content |
| `body-medium` | 14px | 500 | 1.6 | Emphasized body text |
| `small` | 12px | 400 | 1.5 | Metadata, timestamps |
| `caption` | 11px | 500 | 1.4 | Labels, overlines |
| `mono` | 13px | 400 | 1.5 | Data, IDs, code. Use `'SF Mono', 'Consolas', monospace` |

### Rules
- **Never use ALL CAPS for section headers.** Sentence case only. All caps is reserved for small labels (11px caption weight-500).
- **Bold sparingly.** Weight 600 for headings, 500 for emphasis. Never 800 or 900.
- **Letter-spacing:** Only on caption labels: `0.04em`. Nowhere else.

---

## Spacing

Use a 4px base grid. Standard spacing increments:

| Token | Value | Usage |
|-------|-------|-------|
| `space-xs` | 4px | Tight gaps, inline spacing |
| `space-sm` | 8px | Between related items |
| `space-md` | 16px | Card padding, section gaps |
| `space-lg` | 24px | Between sections |
| `space-xl` | 32px | Page-level spacing |
| `space-2xl` | 48px | Major section breaks |

### Rules
- Card internal padding: `20px` (5 * base)
- Gap between cards: `12px`
- Page horizontal padding: `24px`
- Page max-width: `960px` centered

---

## Components

### Cards
```
background: #FFFFFF
border: 1px solid #E0DED8
border-radius: 8px
padding: 20px
box-shadow: none (flat by default)
hover: background #FAFAF7, border #C5C3BC (only if clickable)
```

Cards are the primary container. They are flat — no shadows by default. Subtle border only. Hover state is a slight background shift and border darken, not a lift or shadow.

### Buttons

**Primary:**
```
background: #3D6B50
color: #FFFFFF
border: none
border-radius: 6px
padding: 8px 16px
font-size: 13px
font-weight: 600
hover: background #4E8A65
```

**Secondary:**
```
background: transparent
color: #3D6B50
border: 1px solid #E0DED8
border-radius: 6px
padding: 8px 16px
font-size: 13px
font-weight: 600
hover: background #F2F7F4
```

**Text/Link:**
```
color: #3D6B50
font-weight: 600
text-decoration: none
hover: text-decoration underline
```

### Badges / Tags
```
display: inline-flex
padding: 2px 8px
border-radius: 4px
font-size: 11px
font-weight: 600
letter-spacing: 0.02em
```

Status badges use the status color system. Category badges use `bg-muted` with `text-secondary`.

**Never use rounded-full (pill) badges.** Subtle 4px radius only.

### Tables
```
header: bg-muted, caption type, uppercase
rows: bg-surface, body type
row-border: 1px solid border-subtle
row-hover: bg-surface-hover
cell-padding: 10px 16px
```

Tables are left-aligned. Numbers are right-aligned. No zebra striping.

### Progress Bars
```
track: bg-muted (#F0EFEA)
fill: status color
height: 4px
border-radius: 2px
```

Thin and subtle. Never taller than 6px.

### Avatars / User Indicators
```
width: 28px (default), 20px (small), 36px (large)
border-radius: 50%
background: user's assigned color
color: #FFFFFF
font-size: 38% of width
font-weight: 600
```

Use initials. No profile photos in prototypes.

### Nav / Tabs
```
Active tab:
  color: text-primary
  font-weight: 600
  border-bottom: 2px solid sage-700

Inactive tab:
  color: text-tertiary
  font-weight: 400
  border-bottom: 2px solid transparent

hover:
  color: text-secondary
```

No icons in nav tabs. Text only. The label is the interface.

### Input Fields
```
background: bg-muted
border: 1px solid border-default
border-radius: 6px
padding: 8px 12px
font-size: 14px
focus: border-color sage-600, outline none
```

### Tooltips / Popovers
```
background: #1A1A1A
color: #FFFFFF
border-radius: 6px
padding: 8px 12px
font-size: 12px
max-width: 240px
```

---

## Icons

**Do not use emoji.** Ever. In any Stable Company interface.

Use minimal, functional icons only where a text label is insufficient:
- Chevrons for expand/collapse: `>` `v`
- Arrows for navigation: `→` `←`
- Dot indicators for status: a small colored circle (8px)
- Close: `×`
- Check: `✓` (text character, not an icon)

If you find yourself reaching for an icon library, reconsider whether a text label would work. It almost always does.

---

## Agent Intelligence Display

When surfacing agent-generated insights:

### Inline insights
```
padding: 12px 16px
border-radius: 6px
background: sage-50 (#F2F7F4)
border-left: 3px solid sage-600
font-size: 13px
line-height: 1.6
```

Label the source agent in caption type: `SYNTHESIS · 2h ago` — not with an emoji or bot icon.

### Agent activity feed
Each entry is a single line:
```
[dot color] AGENT NAME — description text                     timestamp
```

Dot colors map to agent tiers:
- Pipeline agents: `text-tertiary` (gray dot)
- Domain specialists: `sage-600` (sage dot)
- Cross-cutters: `status-warn` (amber dot)

---

## Status Patterns

### Rock Status
| Status | Color | Indicator |
|--------|-------|-----------|
| On track | `sage-700` | Filled sage dot |
| At risk | `status-warn` | Filled amber dot |
| Off track | `status-bad` | Filled red-brown dot |
| Complete | `text-tertiary` | Hollow gray dot with checkmark |

### Sentiment (1–5)
Display as a number with a one-word label. Never as stars, hearts, or graphical ratings.
```
4 / 5 — Positive
```

### Health Score
Display as a large number. No circular gauge, no progress ring. The number is the interface.
```
82
Organization Health
```

---

## Layout

### Page Structure
```
[Top nav — sticky, 52px height, bg-surface, bottom border]
[Content — max-width 960px, centered, 24px horizontal padding]
```

### Top Nav
- Left: Logo mark + "Stable OS" in heading type
- Center: Nav tabs (text only, no icons)
- Right: Role toggle + user avatar

### Sidebar (optional for wider layouts)
If used, 200px wide, `bg-primary` background, text-only nav items.

---

## Anti-Patterns — What We Never Do

1. **No emoji in interfaces.** Not in nav, not in headers, not in badges, not anywhere.
2. **No gradient backgrounds.** Flat color only.
3. **No box shadows on cards.** Borders, not shadows.
4. **No pill badges.** Subtle radius (4px).
5. **No color-coded everything.** One accent color (sage) plus status colors. That's it.
6. **No "AI" branding.** Don't label things "AI-powered" or "Smart." The intelligence is implicit.
7. **No exclamation marks in UI copy.** Calm, declarative language.
8. **No loading spinners with cute messages.** Simple "Loading..." or a thin progress bar.
9. **No rounded-full buttons.** Standard 6px radius.
10. **No more than 2 font weights on screen at once.** Usually 400 and 600.

---

## When to Override

This system is the default for all Stable Company tools. Override only when:
- A client's brand requires different colors (swap accent, keep structure)
- A specialized tool has domain-specific conventions (e.g., financial dashboards may need more color coding)
- User testing reveals a specific component isn't working

Document any override with a comment: `// Override: [reason]`
