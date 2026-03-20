# Cortana Brand Guidelines

## Overview

Cortana is a multi-agent AI coordination system built for solo founders and small startups. Our brand reflects our values: **trustworthy, technical, approachable, and efficient**.

---

## Color Palette

### Primary Colors (Trustworthy Tech Blues)

Our primary palette uses blues that convey trust, professionalism, and technical sophistication.

| Token | Hex | Usage |
|-------|-----|-------|
| `cortana-50` | `#f0f9ff` | Light backgrounds, hover states |
| `cortana-100` | `#e0f2fe` | Subtle backgrounds, borders |
| `cortana-200` | `#bae6fd` | Light accents |
| `cortana-300` | `#7dd3fc` | Secondary elements |
| `cortana-400` | `#38bdf8` | Interactive elements |
| `cortana-500` | `#0ea5e9` | Primary brand color |
| `cortana-600` | `#0284c7` | **Primary buttons, links** |
| `cortana-700` | `#0369a1` | Hover states, emphasis |
| `cortana-800` | `#075985` | Dark accents |
| `cortana-900` | `#0c4a6e` | Text on light backgrounds |
| `cortana-950` | `#082f49` | Darkest elements |

### Secondary/Accent Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `purple-500` | `#8b5cf6` | Accent highlights, special features |
| `purple-600` | `#7c3aed` | Accent buttons, CTAs |
| `gray-50` | `#f9fafb` | Section backgrounds |
| `gray-100` | `#f3f4f6` | Borders, dividers |
| `gray-600` | `#4b5563` | Secondary text |
| `gray-900` | `#111827` | Primary text |

### Semantic Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `success` | `#10b981` | Success states, confirmations |
| `warning` | `#f59e0b` | Warnings, cautions |
| `error` | `#ef4444` | Errors, destructive actions |
| `info` | `#3b82f6` | Informational messages |

---

## Typography

### Font Family

- **Primary**: Inter (Google Fonts)
- **Fallback**: `system-ui, -apple-system, sans-serif`

### Type Scale

| Level | Size | Weight | Line Height | Usage |
|-------|------|--------|-------------|-------|
| H1 | `3rem` (48px) | 700 | 1.1 | Hero headlines |
| H2 | `2.25rem` (36px) | 700 | 1.2 | Section headers |
| H3 | `1.5rem` (24px) | 600 | 1.3 | Subsections |
| H4 | `1.25rem` (20px) | 600 | 1.4 | Card titles |
| H5 | `1.125rem` (18px) | 600 | 1.4 | Minor headers |
| H6 | `1rem` (16px) | 600 | 1.5 | Small headers |
| Body | `1rem` (16px) | 400 | 1.6 | Body copy |
| Caption | `0.875rem` (14px) | 400 | 1.5 | Small text, labels |
| Small | `0.75rem` (12px) | 400 | 1.5 | Fine print |

### Typography Principles

- **Readability first**: Generous line-height for body copy
- **Hierarchy clear**: Bold weights for headers, regular for body
- **No all-caps**: Except for very short labels (2-3 words max)
- **Sentence case**: Preferred over title case for headers

---

## Logo Usage

### Primary Logo

The Cortana logo consists of a wordmark with an optional icon.

```
[C icon] Cortana
```

### Logo Variants

1. **Primary**: Blue icon (`cortana-600`) + dark text (`gray-900`)
2. **Monochrome**: All white (for dark backgrounds)
3. **Reversed**: White icon + white text (for dark backgrounds)

### Clear Space

Maintain clear space around the logo equal to the height of the "C" icon on all sides.

### Minimum Size

- **Digital**: 32px height (icon)
- **Print**: 0.5 inches height (icon)

### Don'ts

- ❌ Don't stretch or distort the logo
- ❌ Don't use outdated color variations
- ❌ Don't add effects (drop shadows, gradients)
- ❌ Don't place on busy backgrounds without sufficient contrast

---

## Voice and Tone

### Brand Personality

**Builders helping builders.** We're technical, direct, and empathetic to the founder journey.

### Voice Principles

1. **Direct, not clever**: Say what we mean. No marketing fluff.
2. **Technical, not gatekeeping**: Assume intelligence, explain complexity.
3. **Confident, not arrogant**: We know what we built, but we're learning too.
4. **Empathetic, not patronizing**: We've been in your shoes.

### Tone by Context

| Context | Tone | Example |
|---------|------|---------|
| Hero headlines | Bold, benefit-driven | "Ship faster with AI teammates" |
| Feature descriptions | Clear, specific | "Multi-agent coordination in shared threads" |
| Error messages | Helpful, actionable | "Agent approval required. Review and continue." |
| Documentation | Precise, complete | "The TurnCoordinator manages agent dispatch..." |
| Social media | Human, conversational | "Just shipped: 1,810 passing tests 🎉" |

### Words to Use

- Ship
- Build
- Coordinate
- Control
- Visible
- Approve
- Execute
- Teammates
- Founders
- Builders

### Words to Avoid

- Revolutionary
- Game-changing
- AI-powered (say "multi-agent" instead)
- Enterprise-grade
- Synergy
- Leverage (as a verb)
- Disrupt
- Next-generation

---

## Spacing Scale

We use a consistent spacing scale based on 0.25rem (4px) increments.

| Token | Value | Usage |
|-------|-------|-------|
| `1` | `0.25rem` (4px) | Tight spacing |
| `2` | `0.5rem` (8px) | Icon gaps |
| `3` | `0.75rem` (12px) | Small gaps |
| `4` | `1rem` (16px) | Standard padding |
| `5` | `1.25rem` (20px) | Section padding |
| `6` | `1.5rem` (24px) | Component spacing |
| `8` | `2rem` (32px) | Large gaps |
| `10` | `2.5rem` (40px) | Section margins |
| `12` | `3rem` (48px) | Major sections |
| `16` | `4rem` (64px) | Hero spacing |
| `20` | `5rem` (80px) | Page sections |

---

## Component Guidelines

### Buttons

**Primary Button**
- Background: `cortana-600`
- Text: White
- Hover: `cortana-700`
- Use for: Main CTAs, primary actions

**Secondary Button**
- Background: `cortana-50`
- Text: `cortana-600`
- Hover: `cortana-100`
- Use for: Secondary actions, alternative paths

**Outline Button**
- Border: `cortana-600`
- Text: `cortana-600`
- Hover: `cortana-50`
- Use for: Tertiary actions, cancel buttons

### Cards

- Background: White or `gray-50`
- Border: `gray-100` or subtle shadow
- Padding: `p-6` (24px)
- Border radius: `rounded-xl` (12px)

### Links

- Default: `cortana-600`
- Hover: `cortana-700` + underline
- Visited: Same as default (don't differentiate)

---

## Accessibility

- **Color contrast**: All text meets WCAG AA (4.5:1 for normal text, 3:1 for large text)
- **Focus states**: All interactive elements have visible focus rings
- **Hover states**: Don't rely on hover alone for critical information
- **Alt text**: All images require descriptive alt text
- **Semantic HTML**: Use proper heading hierarchy (H1 → H2 → H3)

---

## Dark Mode (Future)

While not implemented yet, dark mode should use:

- Background: `gray-900` or darker
- Text: `gray-100` for primary, `gray-300` for secondary
- Primary color: `cortana-400` (lighter for contrast)
- Cards: `gray-800`
- Borders: `gray-700`

---

## Design Principles for Target Audience

### For Solo Founders

- **Show value immediately**: First 5 seconds must communicate benefit
- **No fluff**: Get to the point, respect their time
- **Proof it works**: Real examples, screenshots, GitHub stars

### For Small Startups

- **Professional but approachable**: Not enterprise-stiff, not too casual
- **Team-focused**: Show collaboration, not just individual use
- **Scalable messaging**: Works for 2-person or 10-person teams

### Avoid

- ❌ Corporate jargon
- ❌ Complex architecture diagrams (unless in docs)
- ❌ Feature overwhelm (prioritize clarity)
- ❌ Stock photos of "teams collaborating"
- ❌ Animated explainer videos (unless highly polished)

---

*Last updated: 2024 | Version 1.0*
