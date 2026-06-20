---
name: Instagram Photo Optimizer
description: Client-side batch compressor built for Instagram. Drop, compress, post.
colors:
  action-red: "#E1306C"
  action-red-deep: "#c82b61"
  surface-base: "#080808"
  surface-card: "#0f0f0f"
  surface-input: "#111111"
  border-subtle: "#1e1e1e"
  border-moderate: "#2a2a2a"
  border-dropzone: "#252525"
  text-primary: "#e0e0e0"
  text-secondary: "#cccccc"
  text-muted: "#888888"
  text-faint: "#555555"
  status-success: "#4ade80"
  status-warning: "#f59e0b"
  status-error: "#f87171"
typography:
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "20px"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.3px"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.5px"
  caption:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif"
    fontSize: "11.5px"
    fontWeight: 400
    lineHeight: 1.4
rounded:
  xs: "2px"
  sm: "6px"
  md: "7px"
  lg: "8px"
  xl: "11px"
  2xl: "14px"
  pill: "20px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "20px"
  2xl: "24px"
  3xl: "28px"
components:
  button-primary:
    backgroundColor: "{colors.action-red}"
    textColor: "#fefefe"
    rounded: "{rounded.lg}"
    padding: "9px 20px"
  button-primary-hover:
    backgroundColor: "{colors.action-red-deep}"
    textColor: "#fefefe"
    rounded: "{rounded.lg}"
    padding: "9px 20px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.text-faint}"
    rounded: "{rounded.lg}"
    padding: "9px 20px"
  button-ghost-hover:
    backgroundColor: "transparent"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.lg}"
    padding: "9px 20px"
  input-field:
    backgroundColor: "{colors.surface-input}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.md}"
    padding: "7px 10px"
  spec-pill:
    backgroundColor: "{colors.surface-input}"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.pill}"
    padding: "4px 12px"
  photo-card:
    backgroundColor: "{colors.surface-card}"
    textColor: "{colors.text-secondary}"
    rounded: "{rounded.xl}"
    padding: "10px 12px"
---

# Design System: Instagram Photo Optimizer

## 1. Overview

**Creative North Star: "The Darkroom"**

A film photographer's workspace after midnight. Light is minimal. Surfaces are deeply dark, not dramatically black. The one source of color in the room is the safelight: Action Red (#E1306C), glowing just enough to mark what's actionable. Everything else recedes into tonal dark: Surface Base (#080808) beneath Surface Card (#0f0f0f) beneath Surface Input (#111111). Depth comes from layered darkness, not from shadow.

Typography is system-native sans. No web font loading, no Google Fonts CDN request. The stack (-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui) is honest, instant, and renders correctly in under 1ms on every OS. Speed is the product; the font stack is a design decision that proves it.

Status colors are sealed. Success green (#4ade80) means a file is ready. Warning amber (#f59e0b) means the aspect ratio needs attention. Error red (#f87171) means processing failed. None of these colors appear outside their semantic role. They are information, not decoration.

**Key Characteristics:**
- Deep dark surfaces in graduated tones; warmth comes from tonal variation, not a brand color
- Action Red is the only saturated moment on any screen; its rarity is what makes it directional
- System-native typography: fast, honest, zero pretension
- Flat by default: no shadows, no blur. Depth is tonal
- Status colors are sealed to their semantic role, never stylistic

## 2. Colors: The Darkroom Palette

Near-monochrome foundation with one warm action signal. Every surface is a shade of near-black; every piece of text is a shade of near-white. Action Red is the only departure from this tonal logic.

### Primary
- **Action Red** (#E1306C, oklch(55% 0.22 358)): The single saturated signal. Used on: primary button fill, input focus rings, drop zone hover border, browse link text, progress fill. Appears on ≤10% of any screen. Never used for success, warning, decorative highlight, or any semantic purpose beyond "act here."
- **Action Red Deep** (#c82b61, oklch(48% 0.22 358)): Hover and pressed state of Action Red only. Not used independently.

### Neutral
- **Surface Base** (#080808): Root background. Body fills with this. One step above pure black.
- **Surface Card** (#0f0f0f): Photo card backgrounds. One step lighter than Surface Base.
- **Surface Input** (#111111): Input fills, spec pill backgrounds. Third tonal layer.
- **Border Subtle** (#1e1e1e): Card borders at rest. The thinnest perceptible edge.
- **Border Moderate** (#2a2a2a): Input borders, download button border. Slightly more present.
- **Border Dropzone** (#252525): Drop zone dashed border. Between Subtle and Moderate.
- **Text Primary** (#e0e0e0): Body copy, input values. The brightest text the UI uses.
- **Text Secondary** (#cccccc): Card filenames. One step dimmer than Text Primary.
- **Text Muted** (#888888): Spec pill labels, minor secondary text.
- **Text Faint** (#555555): Header subtitle, settings labels, ghost button default.

### Semantic (status contexts only)
- **Status Success** (#4ade80): Compressed file size display and "Ready" label. Appears only when a file completes successfully.
- **Status Warning** (#f59e0b): Aspect ratio out-of-range warning text. Never decorative.
- **Status Error** (#f87171): Failed processing label. Never decorative.

### Named Rules
**The Safelight Rule.** Action Red appears on ≤10% of any screen. Buttons, focus rings, hover borders: that's the entire permitted surface area. The moment it appears on a card background, a heading, or an informational badge, the signal collapses. Its rarity is what makes it actionable.

**The Sealed Status Rule.** Status colors are sealed to their semantic role. A success-green button is prohibited. An amber heading is prohibited. If a color means "done," it appears only when something is done.

## 3. Typography

**Body Font:** System-native sans-serif (-apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif)

**Character:** One typeface family. No display font, no mono accent, no web font. The system stack is the choice: it communicates that this tool cares about loading speed more than typographic personality. That restraint is the personality.

### Hierarchy
- **Headline** (600 weight, 20px, line-height 1.3, letter-spacing -0.3px): Page title only. One instance. The tight tracking gives it presence without requiring large size.
- **Body** (400 weight, 14px, line-height 1.5): Drop zone instructions, card-level reading text.
- **Caption** (400 weight, 11.5px, line-height 1.4): Spec pills, file size numbers, status labels, dimension strings. Dense information layer.
- **Label** (400 weight, 11px, line-height 1, letter-spacing +0.5px, uppercase): Settings field labels only. Uppercase treatment is reserved for form labels.

### Named Rules
**The No-Uppercase-Except-Labels Rule.** Uppercase with positive letter-spacing is reserved strictly for `<label>` elements in settings fields. It marks a structural metadata role. Applying it to headings, buttons, or status text breaks the semantic contract and looks affected.

## 4. Elevation

This system is flat. No `box-shadow` exists anywhere in the codebase. Depth is expressed through tonal layering: Surface Base sits below Surface Card sits below Surface Input. Each step is 1 to 2 lightness increments apart — enough for the eye to register depth without any shadow rendering.

State transitions use color shifts (0.15-0.25s ease), never shadow appearance or blur. The drop zone hover is a border-color shift and a near-invisible background tint; the button hover is a background darkening. Nothing lifts.

**The No-Shadow Rule.** Shadows are prohibited. If the urge arises to add `box-shadow`, reconsider the tonal relationship between surfaces instead. The only legitimate hover feedback is color shift.

## 5. Components

### Buttons
Gently rounded (8px radius), never pill-shaped. Two variants: Primary (act) and Ghost (escape).

- **Primary:** Action Red (#E1306C) fill, near-white (#fefefe) text, 9px/20px padding, 8px radius. Hover: background shifts to Action Red Deep (#c82b61) in 0.15s. Disabled: 0.4 opacity, `not-allowed` cursor.
- **Ghost:** Transparent fill, Text Faint (#555555) text, 1px solid #222222 border. Hover: text shifts to Text Muted (#888888), border to #333333. No background appears on hover.
- **Focus:** Both variants show a 2px Action Red outline at 2px offset on `:focus-visible`.

### Spec Pills
Read-only metadata above the drop zone. Pill radius (20px), Surface Input background, 1px Border Subtle border. Label text in Text Muted; value text in Text Secondary. Never interactive. Never colored. The pill shape and the restraint signal "metadata, not action."

### Drop Zone
Primary interaction surface. 2px dashed Border Dropzone (#252525) border, 14px radius, 52px vertical / 24px horizontal padding. Drag-over and hover: border shifts to Action Red, background tints rgba(225, 48, 108, 0.04) — barely visible warmth, not a fill. The camera emoji (📷) and browse link use the same rhythm. Browse link text is Action Red.

### Photo Cards
Auto-fill grid, 190px minimum column, 12px gap. Surface Card (#0f0f0f) background, 11px radius, 1px Border Subtle at rest. Thumbnail: 1:1 aspect ratio, Surface Thumb (#050505) background, `object-fit: contain`. Done state: border shifts to #1a2e1a (very dark green — implies success without using the full Status Success green). Error state: border shifts to #2e1a1a.

Card body: 10px top, 12px horizontal/bottom padding. Name truncates with `text-overflow: ellipsis`. Size row shows original (Text Dim: #444444) vs. compressed (Status Success: #4ade80). Dimension string and quality percentage in Text Whisper (#333333).

### Inputs and Selects
Surface Input background, 1px Border Moderate border, 7px radius, 7px/10px padding. Focus: border-color shifts to Action Red. No glow, no shadow. 140px fixed width. Settings bar is `flex-wrap: wrap` — controls reflow to new line on narrow viewports.

### Progress Bar
3px height, Surface Progress (#1a1a1a) background, 2px radius. Fill: Action Red, width transitions 0.25s ease. Hidden (`display: none`) between sessions. Appears immediately when processing starts.

### Download Button (per-card)
Surface Dl-Btn (#181818) background, 1px Border Moderate border, 6px radius. Appears only when card state is "done" (`display: block`). Full card-body width, 5px vertical padding. Caption typography. Hover: background #222222, text shifts to Text Primary (#e0e0e0).

## 6. Do's and Don'ts

### Do:
- **Do** use Action Red exclusively for interactive signals: primary buttons, input focus rings, drop zone hover, progress fill, and browse link text.
- **Do** use tonal surface layering for depth: Surface Base → Surface Card → Surface Input in that order. Never reverse the stack.
- **Do** use status colors strictly for processing outcomes: success on completion, warning on ratio mismatch, error on failure.
- **Do** keep focus states visible via Action Red border outline. Keyboard users see the same signal as pointer users.
- **Do** show original size, compressed size, and quality percentage on every processed card. The transparency is a feature.
- **Do** use system-native typography. No web font imports. The page should be fully styled before any network request completes.

### Don't:
- **Don't** use Action Red on card backgrounds, headings, status badges, or decorative dividers. It is a signal, not a theme color.
- **Don't** add `box-shadow`, `backdrop-filter`, or `drop-shadow` anywhere. This system is flat. Depth is tonal.
- **Don't** apply uppercase letter-spacing outside `<label>` elements. It is a structural marker reserved for form fields.
- **Don't** use status colors (success green, warning amber, error red) in any context other than processing state. No green buttons. No amber headings.
- **Don't** animate CSS layout properties (height, width, padding, grid columns). Animate opacity, color, and transform only.
- **Don't** nest cards inside cards. The photo grid is one level deep.
- **Don't** introduce sidebars, modals, drawers, or global navigation. This is a single-surface tool. More chrome increases distraction and undermines the speed principle.
- **Don't** add glassmorphism, blurs, gradients on text, or pixel-perfect light effects. The Darkroom has no frosted glass.
