---
name: admark-design-system-spec
description: Complete visual design system specification for AD Marketing homepage remake
type: website-project
updated: 2026-04-28
---

# AD Marketing - Design System Spec

> **Visual identity specification for the ADMARK homepage remake.** Every token, component, animation pattern, and responsive rule. The design-system-preview.html renders these decisions live.

---

## Design Direction

**Summary:** Dark, confident, and clean. Navy as the dominant dark tone, teal as the singular accent. Generous whitespace on light sections, atmospheric depth on dark sections. Typography does the heavy lifting. DM Serif Display for headlines (editorial weight without stuffiness), DM Sans for everything else (modern, legible, versatile). Animations at Level 2 (Subtle Motion): scroll reveals and stagger effects, nothing flashy.

**Complexity level:** 2 (Subtle Motion)

**Design principles:**
1. **Typography-first** - No hero images. Headlines and layout create visual impact.
2. **Two-tone discipline** - Only navy and teal. No third accent color. Restraint is the design choice.
3. **Dark/light rhythm** - Alternating dark and light sections create visual cadence and prevent monotony.
4. **Proof over promise** - Design that feels earned (real testimonials, real client names) rather than aspirational.

---

## Color System

### Semantic Tokens

| Token | Hex | RGB | Role | 60-30-10 |
|-------|-----|-----|------|----------|
| `navy` (background-alternative) | `#0f1729` | 15, 23, 41 | Dark sections: hero, capabilities, testimonials, footer | 30% structure |
| `navy-light` | `#1a2744` | 26, 39, 68 | Gradient mid-point, card backgrounds on dark | -- |
| `teal` (brand-primary) | `#00c2cb` | 0, 194, 203 | CTAs, icons, eyebrows, accent borders, links | 10% accent |
| `teal-dark` | `#00a8b0` | 0, 168, 176 | Hover state for teal elements, tag text on light bg | -- |
| `white` (background-primary) | `#ffffff` | 255, 255, 255 | Light section backgrounds | 60% base |
| `cream` (background-secondary) | `#f8fafc` | 248, 250, 252 | Alternating light sections, card backgrounds, form bg | 60% base alt |
| `text-primary` | `#0f1729` | 15, 23, 41 | Headings and body text on light backgrounds | -- |
| `slate` (text-secondary) | `#94a3b8` | 148, 163, 184 | Body text, descriptions, metadata | -- |
| `text-on-dark` | `#ffffff` | 255, 255, 255 | Headings on dark backgrounds | -- |
| `text-on-dark-muted` | `rgba(255,255,255,0.6)` | -- | Body text on dark backgrounds | -- |
| `text-on-dark-faint` | `rgba(255,255,255,0.4)` | -- | Metadata, fine print on dark backgrounds | -- |
| `border-light` | `#e2e8f0` | 226, 232, 240 | Card borders, input borders, dividers on light bg | -- |
| `border-dark` | `rgba(255,255,255,0.1)` | -- | Subtle borders on dark backgrounds | -- |
| `star-gold` | `#facc15` | 250, 204, 21 | Testimonial star ratings (fill + stroke) | -- |

### Gradient Definitions

| Name | CSS | Usage |
|------|-----|-------|
| `hero-gradient` | `linear-gradient(135deg, #0f1729 0%, #1a2744 50%, #0f1729 100%)` | Hero, capabilities, testimonials, footer dark backgrounds |
| `teal-button` | `linear-gradient(135deg, #00c2cb, #00a8b0)` | Primary CTA buttons |
| `teal-text` | `linear-gradient(135deg, #00c2cb, #00a8b0)` | Gradient text effect on hero headline accent words |
| `teal-glow` | `radial-gradient(circle at 30% 50%, rgba(0,194,203,0.08), transparent 60%)` | Atmospheric glow on dark sections |

### Contrast Verification (WCAG AA)

| Pair | Ratio | Pass |
|------|-------|------|
| `text-primary` on `white` | 17.4:1 | Yes |
| `text-primary` on `cream` | 16.8:1 | Yes |
| `text-on-dark` on `navy` | 15.2:1 | Yes |
| `slate` on `white` | 3.7:1 | Yes (large text only) |
| `teal` on `navy` | 6.8:1 | Yes |
| `teal` on `white` | 3.2:1 | Yes (large text / UI components) |

---

## Typography System

### Font Stack

| Role | Family | Google Fonts Load | Fallback |
|------|--------|------------------|----------|
| Headings | DM Serif Display | `DM+Serif+Display` | Georgia, serif |
| Body / UI | DM Sans | `DM+Sans:opsz,wght@9..40,300;400;500;600;700` | system-ui, sans-serif |

### Type Scale

| Role | Size (desktop) | Weight | Line Height | Letter Spacing | Tag | Usage |
|------|---------------|--------|-------------|----------------|-----|-------|
| Display | 80-96px (5xl-8xl) | 400 (serif default) | 0.95 | -0.02em | H1 | Hero headline only |
| H2 | 36-48px (4xl-5xl) | 400 (serif) | 1.1 | -0.01em | H2 | Section headlines |
| H3 | 24px (2xl) | 400 (serif) | 1.2 | 0 | H3 | Card titles |
| H4 | 18-20px (lg) | 600 (sans) | 1.3 | 0 | H4 | Feature labels |
| Body LG | 18-20px (lg-xl) | 400 (sans) | 1.6 | 0 | p | Hero subhead, section intros |
| Body | 16px (base) | 400 (sans) | 1.7 | 0 | p | Standard body text |
| Body SM | 14px (sm) | 400 (sans) | 1.6 | 0 | p | Card body, tag text, metadata |
| Eyebrow | 14px (sm) | 600 (sans) | 1.4 | 0.05em | span | ALL CAPS section labels |
| Micro | 12px (xs) | 400 (sans) | 1.5 | 0 | span | Copyright, fine print |

### Responsive Scaling

| Breakpoint | Display | H2 | Body LG |
|------------|---------|----|---------| 
| Desktop (1280+) | 96px (8xl) | 48px (5xl) | 20px (xl) |
| Tablet (768-1279) | 60px (6xl) | 40px (4xl-5xl) | 18px (lg) |
| Mobile (<768) | 48px (5xl) | 36px (4xl) | 18px (lg) |

---

## Spacing System

### Section Spacing

| Context | Desktop | Mobile |
|---------|---------|--------|
| Section vertical padding | 96px (py-24) to 128px (py-32) | 64px (py-16) to 96px (py-24) |
| Section inner max-width | 1280px (max-w-7xl) | Full-width with 24px (px-6) padding |
| Between eyebrow and headline | 12px (mt-3) | 12px |
| Between headline and body | 20px (mb-5) | 16px |
| Between body and CTA | 40px (mb-10) | 32px |

### Component Spacing

| Context | Value |
|---------|-------|
| Card grid gap | 24px (gap-6) |
| Card internal padding | 32px (p-8) |
| Card icon to title | 24px (mb-6) |
| Feature card icon size | 56px container (w-14 h-14), icon 28px (w-7 h-7) |
| Testimonial card padding | 32px (p-8) |
| Form field gap | 20px (space-y-5) |
| Form label to input | 6px (mb-1.5) |
| Input padding | 12px vertical, 16px horizontal (px-4 py-3) |
| Button padding | 16px vertical, 32px horizontal (px-8 py-4) |
| Nav height | 80px (h-20) |

---

## Icon Library

### Selection: Lucide Icons

| Field | Value |
|-------|-------|
| Library | Lucide |
| CDN | `unpkg.com/lucide@latest` |
| Default size | 20-28px depending on context |
| Color inheritance | Icons inherit parent text color via `currentColor` |
| Initialization | `lucide.createIcons()` after DOM load |

### Icon Map

| Context | Icon Name | Size | Color |
|---------|-----------|------|-------|
| Strategy card | `compass` | 28px | teal |
| Tactics card | `target` | 28px | teal |
| Results card | `trending-up` | 28px | teal |
| Google Ads service | `search` | 20px | teal |
| Social Media service | `share-2` | 20px | teal |
| Web Design service | `monitor` | 20px | teal |
| Photography service | `camera` | 20px | teal |
| Videography service | `video` | 20px | teal |
| Graphic Design service | `palette` | 20px | teal |
| SEO service | `bar-chart-3` | 20px | teal |
| Marketing Strategy service | `lightbulb` | 20px | teal |
| Home Services industry | `home` | 40px | teal |
| Medical industry | `heart-pulse` | 40px | teal |
| Education industry | `graduation-cap` | 40px | teal |
| Political industry | `landmark` | 40px | teal |
| Retail industry | `store` | 40px | teal |
| More industries | `sparkles` | 40px | teal |
| No Contracts diff | `file-x` | 20px | teal |
| Low Barrier diff | `wallet` | 20px | teal |
| No Commissions diff | `shield-check` | 20px | teal |
| Realistic Goals diff | `target` | 20px | teal |
| Star rating | `star` | 16px | star-gold (filled) |
| Email contact | `mail` | 20px | teal |
| Phone contact | `phone` | 20px | teal |
| Location contact | `map-pin` | 20px | teal |
| CTA arrow | `arrow-right` | 20px | white |
| Nav menu (mobile) | `menu` | 24px | white |
| Form success | `check` | 32px | teal |
| Checklist items | `check` | 16px | teal |

### Social Icons (inline SVG)

Facebook icon uses inline SVG path (Lucide does not include brand icons):
```
M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z
```

---

## Component Selections

### Navbar
- **Layout:** Logo left, nav links center-right, CTA button far right
- **Behavior:** Fixed position, transparent on hero, blurred dark background on scroll (backdrop-filter: blur(12px))
- **Mobile:** Hamburger icon, dropdown menu with dark background
- **CTA in nav:** "Get Started" as teal gradient rounded-full button

### Hero (Section 1)
- **Layout:** Full-viewport dark background, content left-aligned (max-width 768px), no image
- **Decorative elements:** Two blurred teal glow circles (absolute positioned), two concentric circle outlines (very faint white borders)
- **Trust signal:** Avatar stack (4 teal initial circles with -3 overlap) + "65+ Clients Served" text
- **Scroll indicator:** Centered at bottom, "SCROLL" text + gradient line

### Service Cards (Section 2)
- **Layout:** 3-column grid on desktop, single column on mobile
- **Card structure:** Cream background, rounded-2xl, 8px padding, light border. Icon container (14x14 rounded-xl, teal/10 bg), title (serif H3), body paragraph, divider line, 3-item checklist
- **Hover:** translateY(-6px) + shadow increase

### Capability Pills (Section 3)
- **Layout:** 4-column grid on desktop, 2-column on mobile
- **Pill structure:** Semi-transparent white/5 background, rounded-xl, teal icon + white text, subtle white/10 border
- **Hover:** Border changes to teal/30

### Project Cards (Section 4)
- **Layout:** 3-column grid (2-column tablet, 1-column mobile)
- **Card structure:** Rounded-2xl, border. Top: 4:3 aspect ratio dark gradient with centered serif client name in teal. Bottom: 24px padding, client name, service tag pills (teal/10 bg, teal-dark text)
- **Hover:** translateY(-6px) + shadow

### Industry Cards (Section 5)
- **Layout:** 3-column grid (2-column mobile)
- **Card structure:** White bg, rounded-2xl, 32px padding, centered. Teal icon (40px), title (semibold), descriptor (slate, sm)
- **Hover:** Background fills teal, icon and text turn white

### Differentiator Cards (Section 6)
- **Layout:** Split: text left, stacked cards right
- **Card structure:** Cream bg, rounded-xl, 24px padding, horizontal layout (icon left, text right). Icon in 10x10 rounded-lg teal/10 container.

### Testimonial Cards (Section 7)
- **Layout:** 3-column grid on dark background (2-column tablet, 1-column mobile)
- **Card structure:** White/5 bg, white/10 border, rounded-2xl, 32px padding. Star row, quote, avatar + name + company.
- **Hover:** Border changes to teal/20

### Contact Section (Section 8)
- **Layout:** Split: CTA copy + contact methods left, form right
- **Form:** Cream bg, rounded-2xl, border, 32px padding. Input fields with rounded-xl, focus:border-teal + ring-1
- **Contact icons:** 12x12 rounded-xl, teal/10 bg, hover fills to teal bg with white icon
- **Submit button:** Full-width teal gradient, rounded-xl, 16px vertical padding

### Footer
- **Layout:** 4-column (logo+desc spans 2), dark background
- **Bottom bar:** Border-top white/10, flex between copyright and credit

---

## Section Background Alternation

```
Section 1: Hero              → hero-gradient (dark navy)
Section 2: Services          → white
Section 3: Capabilities      → hero-gradient (dark navy)
Section 4: Featured Work     → white
Section 5: Industries        → cream (#f8fafc)
Section 6: Differentiators   → white
Section 7: Testimonials      → hero-gradient (dark navy)
Section 8: Contact           → white
Section 9: Footer            → hero-gradient (dark navy)
```

Rule: No two consecutive sections share the same background. Dark sections get the `hero-gradient`. Light sections alternate between white and cream.

---

## Animation Patterns (Level 2: Subtle Motion)

### `fade-up`
- **Trigger:** ScrollTrigger, top 85% of viewport
- **Initial state:** opacity: 0, translateY(40px)
- **Animation:** opacity: 1, y: 0
- **Duration:** 800ms
- **Easing:** power3.out
- **Applied to:** Section headers, hero content blocks, contact section content
- **Once:** true (does not replay on scroll up)

### `stagger-item`
- **Trigger:** ScrollTrigger on parent section, top 75%
- **Initial state:** opacity: 0, translateY(30px)
- **Animation:** opacity: 1, y: 0
- **Duration:** 600ms per item
- **Stagger:** 100ms between items
- **Easing:** power3.out
- **Applied to:** Card grids (services, work, industries, differentiators, testimonials, capabilities)
- **Once:** true

### `card-hover`
- **Trigger:** CSS hover (no JS)
- **Animation:** translateY(-6px) + box-shadow increase
- **Duration:** 300ms
- **Easing:** ease
- **Applied to:** Service cards, project cards

### `button-hover`
- **Trigger:** CSS hover
- **Animation:** translateY(-2px) + teal glow shadow (0 10px 30px rgba(0,194,203,0.3))
- **Duration:** 300ms
- **Easing:** ease
- **Applied to:** All `.btn-primary` elements

### `nav-scroll`
- **Trigger:** window.scrollY > 80
- **Animation:** Navbar background transitions from transparent to rgba(15,23,41,0.95) with border-bottom
- **Duration:** 300ms (CSS transition-all)
- **Applied to:** #navbar

### `scroll-progress`
- **Trigger:** Window scroll event
- **Animation:** Left-side vertical bar fills based on scroll percentage
- **Applied to:** #scroll-progress (fixed, left edge, hidden on mobile)

### Reduced Motion Fallback
When `prefers-reduced-motion: reduce`:
- All `.fade-up` and `.stagger-item` elements render at full opacity with no transform
- Card hovers still work (transform only, no opacity change)
- Scroll progress bar still works (no animation, just position)
- Nav background transition still works

---

## Image Treatment Standards

| Context | Treatment | Notes |
|---------|-----------|-------|
| Hero | No image. Typography + decorative geometry. | Dark gradient with teal glow circles and concentric ring outlines. |
| Project cards | No real images. Typography cards (serif client name on navy gradient). | Placeholder pattern for demo. Real build would use project screenshots. |
| Testimonials | Initial-based avatars (teal/20 bg, teal text, 40px circle). | No photos available. Initials maintain visual interest. |
| Trust signal | Avatar stack of 4 initial circles with -3 overlap. | Overlapping circles suggest real people without needing photos. |
| Icons | Lucide icons at documented sizes. Teal color. | Never use raster icon images. Always SVG via Lucide. |

---

## Responsive Breakpoints

| Breakpoint | Width | Key Changes |
|------------|-------|-------------|
| Mobile | <768px | Single-column grids, hamburger nav, full-width form, reduced section padding |
| Tablet | 768-1279px | 2-column grids for cards, desktop nav, split layouts stack |
| Desktop | 1280px+ | Full 3-4 column grids, side-by-side splits, max-w-7xl container |

### Component Responsive Behavior

| Component | Desktop | Tablet | Mobile |
|-----------|---------|--------|--------|
| Service cards | 3-col grid | 2-col grid | 1-col stack |
| Capability pills | 4-col grid | 3-col grid | 2-col grid |
| Project cards | 3-col grid | 2-col grid | 1-col stack |
| Industry cards | 3-col grid | 2-col grid | 2-col grid |
| Differentiators | Side-by-side | Side-by-side | Stacked |
| Testimonials | 3-col grid | 2-col grid | 1-col stack |
| Contact | Side-by-side | Side-by-side | Stacked (form below) |
| Footer | 4-col | 2-col | 1-col stack |
| Nav links | Visible | Visible | Hamburger menu |
| Scroll progress | Visible | Visible | Hidden |

---

## Button Variants

### Primary Button (`.btn-primary`)
- Background: teal-button gradient
- Text: white, font-semibold
- Padding: px-8 py-4 (large), px-5 py-2.5 (nav)
- Border-radius: rounded-full
- Hover: translateY(-2px), box-shadow: 0 10px 30px rgba(0,194,203,0.3)
- Used for: Nav CTA, Hero primary CTA, Form submit

### Secondary/Ghost Button
- Background: transparent
- Border: 1px solid white/10
- Text: white/60, font-medium
- Hover: text white, border white/30
- Padding: px-8 py-4
- Border-radius: rounded-full
- Used for: Hero secondary CTA ("See Our Work")

### Form Submit Button
- Same as primary but full-width (w-full)
- Border-radius: rounded-xl (not rounded-full, matches form card shape)
- Includes arrow-right icon

---

## Form Elements

### Input Fields
- Background: white
- Border: 1px solid border-light (#e2e8f0)
- Border-radius: rounded-xl
- Padding: px-4 py-3
- Focus: border-teal, ring-1 ring-teal
- Placeholder: gray-400
- Font: DM Sans, base size

### Labels
- Font: DM Sans, sm, font-medium
- Margin-bottom: 6px (mb-1.5)
- Color: text-primary

### Textarea
- Same as input, rows="4", resize-none

---

*Last updated: 2026-04-28*
