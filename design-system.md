# Gridicity Design System
*Extracted from dd94873e Fleet TCO Calculator — source of truth is `frontend/src/pages/tco/HomePage.tsx` and `frontend/src/main.css` (latest commit a3c7fa9)*

---

## Colours

| Token | Hex | Usage |
|---|---|---|
| Background | `#f5fbf7` | Page background |
| Surface / Card | `#ffffff` | Card backgrounds |
| Foreground (headings) | `#0e1c17` | Main text, headings |
| Foreground muted | `rgba(14,28,23,0.55)` | Body/sub text |
| Foreground faint | `rgba(14,28,23,0.30)` | Labels, captions |
| Foreground ultra-faint | `rgba(14,28,23,0.08)` | Card borders |
| Primary action | `#116c4a` | Buttons, selected states, em text |
| Primary hover | `#0d5438` | Hover on primary buttons |
| Primary dark | `#0e1c17` | Dark header buttons, nav |
| Primary dark hover | `#1a2e24` | Hover on dark buttons |
| Border default | `rgba(0,0,0,0.08)` | Card borders (`border-black/8`) |
| Border interactive | `rgba(0,0,0,0.10)` | Selectable item borders |
| Border hover | `rgba(17,108,74,0.40)` | Hover on selectable items |

---

## Typography

| Role | Family | Weight | Size | Notes |
|---|---|---|---|---|
| Page heading (h1) | Poppins | 600 semibold | 48px / 3rem | `tracking-tight`, `leading-[1.1]` |
| Section heading (h2) | Poppins | 700 bold | 32–40px | |
| Sub-heading (h3) | Poppins | 600 semibold | 18–20px | |
| Logo brand name | Poppins | 400 normal | 18px | `letter-spacing: 0.12em`, colour `#116c4a` |
| Logo product name | Poppins | 700 bold | 24px | colour `#0e1c17` |
| Body / UI text | DM Sans | 400 | 16–18px | |
| Labels / form | DM Sans | 600 | 15–16px | |
| Numbers & CTAs | JetBrains Mono | 700 bold | varies | `letter-spacing: 0.06em`, uppercase |
| Small / captions | JetBrains Mono | 400 | 12px | colour `#0e1c17/30` |

---

## Spacing & Radius

| Token | Value |
|---|---|
| Card border-radius | `rounded-2xl` = 16px |
| Button border-radius | `rounded-xl` = 12px |
| Tag / pill border-radius | `rounded-full` |
| Card padding | `p-8` = 32px |
| Section padding | `pt-12 pb-16` |
| Container max-width | `600px` (narrow / centred) |

---

## Shadows

| Token | Value |
|---|---|
| Card shadow | `shadow-sm` = `0 1px 3px rgba(0,0,0,0.12)` |
| Selected state shadow | `shadow-md` = `0px 4px 10px rgba(0,0,0,0.12)` |
| No hover glow effects | — |

---

## Component Patterns

### Header / Navbar
```
bg-white | border-b border-black/8 | px-10 py-6
Logo: img + "Gridicity" (Poppins 400 #116c4a letter-spacing:0.12em) + "Fleet TCO" (Poppins 700 #0e1c17)
Nav CTA: bg-[#0e1c17] text-white rounded-xl px-6 py-3 | JetBrains Mono uppercase | hover:bg-[#1a2e24]
```

### Card
```
bg-white rounded-2xl border border-black/8 shadow-sm p-8
```

### Primary Button (CTA)
```
bg-[#116c4a] hover:bg-[#0d5438] text-white
rounded-xl | h-14 | text-[15px] font-semibold
JetBrains Mono | letter-spacing:0.06em | uppercase
disabled:opacity-35
```

### Selectable Button (active)
```
bg-[#116c4a] border-[#116c4a] text-white shadow-md rounded-xl
```

### Selectable Button (inactive)
```
bg-white border-black/10 text-[#0e1c17]/70 rounded-xl
hover:border-[#116c4a]/40 hover:text-[#0e1c17]
```

### Emphasis text (`<em>`)
```
not-italic text-[#116c4a]
```

### Numeric display
```
text-xl font-bold text-[#116c4a] | JetBrains Mono
```

---

## Gradients (from main.css — used on darker panels only)

| Name | Value |
|---|---|
| Hero gradient | `linear-gradient(135deg, #1b4332 0%, #012d1d 100%)` |
| Accent gradient | `linear-gradient(135deg, #116c4a 0%, #1b4332 100%)` |
| Success gradient | `linear-gradient(135deg, #116c4a 0%, #40916c 100%)` |

*Note: The homepage itself does NOT use the dark hero gradient — that's reserved for the results/dashboard panels. The landing page is light (#f5fbf7 bg, white cards).*

---

## Overall Aesthetic

- **Minimal, clean, airy** — very little visual noise
- White cards on a pale green background
- Borders are ultra-subtle (`border-black/8`)
- Shadows are small and soft
- Colour accent (`#116c4a`) appears only on interactive/active states and key headings
- Monospace font (JetBrains Mono) is a distinctive character marker for numbers and CTAs
- No gradients on the main landing surface — gradients appear inside dashboard/results panels
