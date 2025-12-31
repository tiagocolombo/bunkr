# Bunkr Design System

**Philosophy:** Ruthlessly simple. Every decision optimized for non-tech-savvy users (50+). No design for design's sake.

---

## Brand Identity

### Name
**Bunkr** — A secure bunker for your passwords.

### Tagline Options
- "Segurança simples para todo mundo" - yes, we want a Portuguese-BR version
- "Your passwords, protected"
- "Security made simple"

### Brand Personality
- **Trustworthy** — Like a bank vault, but friendly
- **Simple** — No jargon, no complexity
- **Approachable** — Not intimidating or techy
- **Reliable** — Always there when you need it

---

## Core Principles

### 1. Clarity Over Cleverness
- No hidden gestures
- Explicit labels on everything
- Clear call-to-action buttons
- No ambiguous icons without text

### 2. Accessibility First
- WCAG AAA compliance (7:1 contrast)
- Minimum 16px font size (18px preferred)
- Large touch targets (minimum 48px)
- Works with screen readers

### 3. Forgiving UX
- Undo everything non-destructive
- Confirmation dialogs for dangerous actions
- Autosave whenever possible
- Clear error messages with solutions

### 4. Progressive Disclosure
- Simple by default
- Advanced features clearly labeled as "Advanced"
- No technical jargon in main flows

---

## Color Palette

### Purpose: High contrast, accessible, calming (not alarming)

```
Primary (Blue - Trust & Security)
├─ 50:  #EFF6FF  (Backgrounds)
├─ 100: #DBEAFE  (Hover states)
├─ 500: #3B82F6  (Primary actions) ← Main brand color
├─ 600: #2563EB  (Primary hover)
└─ 900: #1E3A8A  (Text on light backgrounds)

Neutral (Grayscale)
├─ 50:  #FAFAFA  (Page backgrounds)
├─ 100: #F5F5F5  (Card backgrounds)
├─ 200: #E5E5E5  (Borders)
├─ 500: #737373  (Secondary text)
├─ 700: #404040  (Body text)
└─ 900: #171717  (Headings)

Semantic Colors
├─ Success: #10B981  (Green - confirmations)
├─ Error:   #EF4444  (Red - warnings)
├─ Warning: #F59E0B  (Amber - cautions)
└─ Info:    #3B82F6  (Blue - tips)
```

**Why these colors?**
- Blue: Universal signal for trust/security
- High contrast ratios for aging eyes
- Not too vibrant (won't fatigue older users)

---

## Typography

### Font Families

**Primary: System Fonts**
```
iOS:     -apple-system, BlinkMacSystemFont
Android: Roboto
Web:     Inter (fallback to system)
```

**Why system fonts?**
- Free
- Optimized for each platform
- Users already familiar
- No download time

**Code/Passwords: Monospace**
```
'SF Mono', 'Roboto Mono', 'Courier New', monospace
```

### Font Sizes

```
┌─────────────┬──────────┬─────────────┬─────────────┐
│ Purpose     │ Size     │ Weight      │ Line Height │
├─────────────┼──────────┼─────────────┼─────────────┤
│ Hero/Title  │ 32px     │ 700 (Bold)  │ 1.2         │
│ H1          │ 24px     │ 600 (Semi)  │ 1.3         │
│ H2          │ 20px     │ 600 (Semi)  │ 1.4         │
│ Body Large  │ 18px     │ 400 (Reg)   │ 1.5         │
│ Body        │ 16px     │ 400 (Reg)   │ 1.5         │
│ Small       │ 14px     │ 400 (Reg)   │ 1.4         │
│ Caption     │ 12px     │ 400 (Reg)   │ 1.3         │
└─────────────┴──────────┴─────────────┴─────────────┘
```

**Critical Rule:** Never use body text smaller than 16px.

---

## Logo Guidelines

### Concept
The Bunkr logo should convey:
- **Security** without being scary
- **Simplicity** — clean, minimal shapes
- **Trust** — stable, grounded

### Style
- Geometric, minimal
- Works at small sizes (app icon, favicon)
- Single color or two-tone max
- No gradients (keeps it timeless)

### Icon Concepts
- Abstract bunker/vault door
- Stylized "B" with shield element
- Lock integrated into letterform
- Keyhole as negative space

---

## Spacing Scale

**Based on 8px grid system:**

```
┌────┬──────┬────────────────────────┐
│ T  │ Size │ Usage                  │
├────┼──────┼────────────────────────┤
│ xs │  4px │ Tight spacing in lists │
│ sm │  8px │ Between related items  │
│ md │ 16px │ Standard spacing       │
│ lg │ 24px │ Between sections       │
│ xl │ 32px │ Large gaps             │
│ 2xl│ 48px │ Page margins           │
└────┴──────┴────────────────────────┘
```

---

## Components

### Button

**Three variants only:**

#### 1. Primary (Main actions)
```
Background: Primary-500 (#3B82F6)
Text: White
Padding: 12px 24px (mobile: 16px 32px)
Border Radius: 8px
Font: 16px, Weight 600
Min Height: 48px

States:
- Hover: Primary-600
- Active: Primary-700
- Disabled: Neutral-200, Text: Neutral-500
- Loading: Show spinner, disable interaction
```

#### 2. Secondary (Alternative actions)
```
Background: Transparent
Border: 2px solid Primary-500
Text: Primary-600
[Same spacing/sizing as Primary]
```

#### 3. Danger (Destructive actions)
```
Background: Error (#EF4444)
Text: White
[Same spacing/sizing as Primary]
```

### Input Fields

```
Height: 48px minimum
Padding: 12px 16px
Border: 2px solid Neutral-200
Border Radius: 8px
Font: 16px

States:
- Focus: Border Primary-500, shadow ring
- Error: Border Error, red helper text
- Disabled: Background Neutral-100
```

### Cards

```
Background: White
Border: 1px solid Neutral-200
Border Radius: 12px
Padding: 16px (mobile: 20px)
Shadow: 0 1px 3px rgba(0,0,0,0.1)
```

---

## Copy Writing Guidelines

### Voice & Tone

**Voice (Consistent):**
- Clear and simple
- Friendly but not cutesy
- Respectful (never condescending)

**Tone (Contextual):**
- Onboarding: Encouraging
- Errors: Helpful, not blaming
- Success: Brief celebration
- Settings: Direct

### Button Labels

**Good:**
- "Save Password"
- "Add to Bunkr"
- "Delete Forever"

**Bad:**
- "Submit" (Submit what?)
- "OK" (What happens?)
- "Delete" (Delete what? Reversible?)

### Microcopy

**Password Strength:**
```
Too short → "Add more characters"
Weak → "Make it stronger"
Good → "That's secure"
Strong → "Excellent!"
```

**Empty States:**
```
"No passwords yet" ✓
"No data available" ✗ (technical)
```

**Errors:**
```
"Couldn't connect to server" ✓
"Network error" ✗ (jargon)
```

---

## Design Tokens (For Implementation)

### CSS Custom Properties

```css
:root {
  /* Brand */
  --brand-name: "Bunkr";

  /* Colors */
  --color-primary: #3B82F6;
  --color-primary-hover: #2563EB;
  --color-success: #10B981;
  --color-error: #EF4444;
  --color-warning: #F59E0B;

  /* Neutrals */
  --color-bg: #FAFAFA;
  --color-card: #FFFFFF;
  --color-border: #E5E5E5;
  --color-text: #404040;
  --color-text-secondary: #737373;

  /* Typography */
  --font-sans: -apple-system, BlinkMacSystemFont, 'Inter', sans-serif;
  --font-mono: 'SF Mono', 'Roboto Mono', monospace;

  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --text-xl: 1.25rem;
  --text-2xl: 1.5rem;

  /* Spacing */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2rem;
  --space-2xl: 3rem;

  /* Radius */
  --radius-sm: 0.5rem;
  --radius-md: 0.75rem;
  --radius-lg: 1rem;

  /* Shadows */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.1);
  --shadow-md: 0 4px 6px rgba(0,0,0,0.1);
  --shadow-lg: 0 20px 25px rgba(0,0,0,0.15);

  /* Transitions */
  --transition-fast: 150ms ease-in-out;
  --transition-base: 200ms ease-in-out;
  --transition-slow: 300ms ease-in-out;
}
```

---

## Design Review Checklist

Before implementing any screen:

- [ ] Can a 50+ year old use this?
- [ ] Are touch targets at least 48px?
- [ ] Is text at least 16px?
- [ ] Is contrast ratio 7:1 or better?
- [ ] Does it work without color (grayscale test)?
- [ ] Can you navigate with keyboard only?
- [ ] Are errors helpful?
- [ ] Is success obvious?
- [ ] Could you remove anything?

**If you answer "no" to any of these, redesign.**

---

## Final Principle

**When in doubt, make it simpler.**

If your grandmother wouldn't understand it, it's too complicated.

🔐 **Bunkr** - Design for trust, implement for clarity.