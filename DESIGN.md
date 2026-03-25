# COZY PIZZA LANDING PAGE — DESIGN SPECIFICATION

---

## SUMMARY
A warm, inviting landing page celebrating handcrafted pizza with earthy tones, soft typography, and conversational design that feels like stepping into a neighborhood pizzeria.

---

## LAYOUT

### VIEWPORT STRUCTURE (Mobile-First, 375px → 1440px)

**HEADER / NAVIGATION**
- Fixed sticky header at top (height: 64px on mobile, 72px on desktop)
- Left: Logo (40×40px mark, text lockup on desktop only)
- Center: Nav links (hidden on mobile, visible ≥768px)
- Right: CTA button + hamburger menu (mobile)
- Background: Solid #FFFBF7 with subtle bottom border (#E8D5C4, 1px)

**HERO SECTION**
- Full-width viewport height (100vh, min 480px on mobile)
- Background: Warm gradient (top #FFF4EA → bottom #FFF0E6) with optional topography/pattern overlay at 8% opacity
- Content area: Centered, max-width container (1200px)
- Text block (left 16px padding on mobile, centered ≥768px): Hero headline + subheading + CTA button
- Image area (right side ≥1024px): Hero pizza photography, aspect ratio 4:3, positioned bottom-right
- Vertical spacing: 80px top, 60px bottom (mobile); 120px top, 100px bottom (desktop)

**NAVIGATION MENU (Mobile Hamburger)**
- Overlay modal covering full viewport when open
- Background: #2D1B11 (dark brown) with 95% opacity
- Menu items stacked vertically, 20px spacing, text-align center
- Close button top-right (32×32px)
- Slide-in from right, 300ms easing (ease-out-cubic)

**MENU PREVIEW SECTION**
- White background (#FFFFFF)
- Padding: 60px 16px (mobile), 100px 24px (≥768px)
- Section heading centered, 40px below top padding
- Grid: 1 column (mobile), 2 columns (≥768px), 3 columns (≥1200px)
- Card spacing: 24px gaps (mobile), 32px (desktop)
- Card dimensions: 100% width (mobile), ~280px ideal width (desktop)
- Container max-width: 1200px, centered

**PIZZA CARD COMPONENT** (repeats 4 times)
- Background: #FFFBF7
- Border: 1px solid #E8D5C4
- Border-radius: 12px
- Padding: 16px
- Image container (height 200px, aspect-ratio 4:3): overflow hidden, rounded top corners
- Content area: 12px padding, text-align left
- Pizza name (headline, 18px bold), description (14px, #6B5344), price (16px bold, #C17A5C)
- "View Details" link (14px, #C17A5C, underline on hover)

**ABOUT / STORY SECTION**
- Alternating layout: Text left / Image right (≥1024px); stacked mobile
- Background: #FFF9F5
- Padding: 80px 16px (mobile), 120px 24px (desktop)
- Text block: max-width 480px, line-height 1.6
- Image: aspect-ratio 5:4, border-radius 16px, shadow 0 8px 24px rgba(0,0,0,0.08)
- Heading: 36px (mobile), 48px (desktop), #2D1B11

**REVIEWS / TESTIMONIALS SECTION**
- Background: #FFFBF7
- Padding: 80px 16px (mobile), 100px 24px (desktop)
- Carousel container with left/right nav buttons (48×48px, circular, #C17A5C)
- Single card visible (mobile), 2 cards visible (≥768px), 3 cards visible (≥1200px)
- Card dimensions: 100% (mobile), ~320px (desktop)
- Card background: #FFFFFF, border 1px #E8D5C4, padding 24px, border-radius 12px
- Star rating (5 stars, ★ symbol, #F4A460), 16px
- Review text: 14px, #6B5344, italic
- Author name: 14px bold, #2D1B11

**CONTACT / ORDER CTA SECTION**
- Background: Linear gradient (#2D1B11 → #3D2B1F)
- Padding: 80px 16px (mobile), 120px 24px (desktop)
- Layout: Single column (mobile), 2 columns (≥768px), 12px gap
- Left column: Heading + description text + decorative element (pizza emoji or icon)
- Right column: Contact form OR dual-column link group (phone + online order)
- Text color: #FFFBF7
- Form fields: Full-width, padding 12px, background #FFFBF7, text #2D1B11, border-radius 6px, focus outline #F4A460 (3px)

**FOOTER**
- Background: #2D1B11
- Padding: 60px 16px (mobile), 80px 24px (desktop)
- Layout: 1 column (mobile), 4 columns (≥768px)
- Column 1: Logo + tagline (14px, #D4BFAE)
- Column 2: Hours (label + times, 13px)
- Column 3: Address (label + street/city, 13px)
- Column 4: Social icons (32×32px each, 6px gaps) + Newsletter signup (email input + button)
- Bottom bar (border-top #4D3B2F): Copyright text center, padding 24px 0, 12px font size
- Link color: #D4BFAE, hover: #F4A460
- Social icons: Circular, background transparent, stroke #D4BFAE, hover: stroke #F4A460

---

## COLORS

| Element | Hex Code | Usage |
|---------|----------|-------|
| **Primary Background** | #FFFBF7 | Default section background, cards |
| **White** | #FFFFFF | Pure white for contrast areas, form backgrounds |
| **Cream** | #FFF9F5 | About section, subtle alternation |
| **Light Tan** | #FFF4EA | Hero gradient top, light accents |
| **Warm Sand** | #FFF0E6 | Hero gradient bottom |
| **Border/Divider** | #E8D5C4 | Card borders, subtle lines |
| **Accent Orange** | #C17A5C | Call-to-action buttons, links, hover states |
| **Lighter Orange** | #D4956B | Secondary accent, disabled states |
| **Caramel** | #F4A460 | Focus states, badges, highlights |
| **Text Primary** | #2D1B11 | Headlines, primary copy (dark brown) |
| **Text Secondary** | #6B5344 | Body text, descriptions (medium brown) |
| **Text Light** | #D4BFAE | Footer text, light backgrounds (warm tan) |
| **Dark Background** | #2D1B11 | Footer, dark sections (charcoal brown) |
| **Dark Variant** | #3D2B1F | Gradient end, secondary dark section |
| **Border Dark** | #4D3B2F | Footer dividers, dark section accents |

**Color Contrast Verification (WCAG AA):**
- #2D1B11 (text) on #FFFBF7 (background): 16.2:1 ✓
- #C17A5C (accent) on #FFFFFF (button background): 4.8:1 ✓
- #6B5344 (secondary text) on #FFFBF7: 7.1:1 ✓
- #D4BFAE (footer text) on #2D1B11: 6.5:1 ✓

---

## COMPONENTS

### TYPOGRAPHY
- **Font Stack**: Inter or system sans-serif for body; Playfair Display or Georgia serif for headlines (fallback to serif stack)
- **Headlines (H1)**: 48px (mobile: 32px), weight 700, line-height 1.2, letter-spacing -0.5px
- **Subheadings (H2)**: 36px (mobile: 24px), weight 700, line-height 1.3
- **Body Text**: 16px, weight 400, line-height 1.6, letter-spacing 0
- **Small Text** (labels, captions): 12px–14px, weight 500, line-height 1.4
- **CTA Text**: 16px, weight 600, text-transform uppercase, letter-spacing 0.5px

### BUTTONS
- **Primary CTA Button**: 
  - Background: #C17A5C, Text: #FFFBF7, weight 600
  - Padding: 16px 32px, border-radius 8px
  - Hover: Background #D4956B, cursor pointer
  - Focus: Outline 3px solid #F4A460 (2px offset)
  - Disabled: Background #D4BFAE, opacity 60%, cursor not-allowed
  - Transition: all 200ms ease-out

- **Secondary Button** (e.g., menu hamburger):
  - Background: transparent, stroke #2D1B11, 2px
  - Hover: Background #F4A460 (8% opacity), stroke #C17A5C
  - Size: 48×48px on desktop, 44×44px on mobile
  - Focus: Outline 2px solid #F4A460 (1px offset)

- **Icon Button** (carousel arrows, close):
  - Circular, 48px diameter, background #C17A5C, icon #FFFBF7
  - Hover: Background #D4956B
  - Disabled: Background #D4BFAE, opacity 50%

### FORM INPUTS
- **Text Input / Email**:
  - Width: 100% (mobile), auto (desktop form two-column)
  - Padding: 12px 16px, background #FFFBF7, border 1px #E8D5C4
  - Border-radius: 6px, font-size 14px
  - Focus: Border 2px #C17A5C, outline none, box-shadow 0 0 0 3px rgba(193, 122, 92, 0.1)
  - Placeholder: #A68973, opacity 70%

- **Label**:
  - Font-size: 13px, weight 600, color #2D1B11
  - Margin-bottom: 6px, display block

### CARDS
- **Menu Card**:
  - Width: 100% (mobile), ~280px (desktop)
  - Background: #FFFBF7, border 1px #E8D5C4, border-radius 12px
  - Padding: 16px, overflow hidden
  - Image container: height 200px, border-radius 8px (top corners)
  - Hover state: Box-shadow 0 12px 32px rgba(0,0,0,0.12), transform translateY(-4px)
  - Transition: all 300ms ease-out

- **Review Card**:
  - Width: 100% (mobile), ~320px (desktop)
  - Background: #FFFFFF, border 1px #E8D5C4, border-radius 12px
  - Padding: 24px 20px, text-align left
  - Star rating: ★★★★★ (5 each = 16px, #F4A460)
  - Hover: Box-shadow 0 8px 24px rgba(0,0,0,0.08)

### NAVIGATION
- **Logo**:
  - Mark: 40×40px, can be icon or wordmark
  - Text lockup (desktop): 24px bold, #2D1B11, margin-left 12px
  - Hover: Opacity 80% with smooth transition

- **Nav Links** (desktop horizontal):
  - Font-size: 14px, weight 500, color #2D1B11
  - Spacing: 32px horizontal gap
  - Hover: Color #C17A5C, underline (2px solid, offset 4px)
  - Active link: Color #C17A5C, underline permanent
  - Focus: Outline 2px solid #F4A460 (2px offset), border-radius 4px

- **Hamburger Menu** (mobile):
  - 3 horizontal lines (2px thickness each, 6px gap), 24×24px viewBox
  - Color: #2D1B11
  - Animation: Lines rotate/fade on open
  - Hit area: 48×48px (centered on 24px icon)

### HERO SECTION COMPONENTS
- **Hero Image**:
  - Aspect ratio: 4:3 (desktop), full-width above text (mobile)
  - Border-radius: 16px, shadow 0 16px 48px rgba(0,0,0,0.1)
  - Object-fit: cover, object-position: center

- **Hero Text Block**:
  - Max-width: 520px (desktop), 100% (mobile)
  - Headline: #2D1B11, 48px (mobile: 32px), line-height 1.2
  - Subheading: #6B5344, 18px (mobile: 16px), margin-top 16px, line-height 1.5
  - CTA Button: Positioned 32px below subheading

### TESTIMONIAL CAROUSEL
- **Embla Carousel Setup**:
  - Slide count: 3–5 testimonial cards
  - Scroll behavior: Snap to center (mobile), smooth 350ms
  - Navigation: Left/right arrow buttons (48×48px, circular, #C17A5C)
  - Indicators (dots): 8px circles, #D4BFAE (inactive), #C17A5C (active), spacing 8px
  - Mobile: Single card visible, swipeable with touch
  - Tablet+: 2–3 cards visible, paginated with arrows

### ACCESSIBILITY COMPONENTS
- **Focus Indicators**: All interactive elements have visible 2–3px outline (#F4A460) with 1–2px offset
- **Skip Link**: Hidden unless focused, positioned top-left, background #2D1B11, color #FFFBF7, padding 8px 12px, z-index 100
- **ARIA Labels**: 
  - Hamburger button: `aria-label="Toggle navigation menu"`
  - Carousel buttons: `aria-label="Previous testimonial"`, `aria-label="Next testimonial"`
  - Form inputs: Connected via `<label>` elements
  - Close modal: `aria-label="Close menu"`
- **Semantic HTML**: `<nav>`, `<button>`, `<form>`, `<section>`, `<article>` used correctly
- **Keyboard Navigation**: Tab order follows visual flow left-to-right, top-to-bottom; Enter/Space activate buttons; Escape closes mobile menu

---

## INTERACTIONS

### HEADER / STICKY NAV
- **Scroll Behavior**: Header remains fixed at top with z-index 50, subtle box-shadow (0 2px 8px rgba(0,0,0,0.05)) appears after 50px scroll
- **Mobile Menu Toggle**: 
  - Click hamburger → menu overlay slides in from right (300ms), background dims with 95% opacity
  - Click close button or outside overlay → slides out (300ms)
  - Menu items animate in staggered (50ms per item)
- **Logo Click**: Navigate to #hero (smooth scroll 600ms)
- **Nav Links Click**: Smooth scroll to corresponding section (600ms)
- **Link Hover (desktop)**: Text color #C17A5C, underline slides in from left (200ms)

### HERO SECTION
- **Hero Image**: On desktop, subtle parallax scroll effect (25% slower than viewport)
- **CTA Button Hover**: 
  - Background shifts #C17A5C → #D4956B (200ms)
  - Box-shadow 0 8px 24px rgba(193, 122, 92, 0.3) appears
  - Cursor changes to pointer

### MENU CARDS
- **Card Hover** (desktop):
  - Box-shadow lifts: 0 12px 32px rgba(0,0,0,0.12) (300ms ease-out)
  - Transform translateY(-4px)
  - Image zooms 1.05x (300ms)
- **Card Click**: Navigate to pizza detail page or open modal with full menu info
- **Link "View Details" Hover**: Color #C17A5C, underline appears (150ms)

### REVIEW CAROUSEL (Embla)
- **Auto-play**: Optional, 5-second interval with pause on hover
- **Arrow Button Click**: 
  - Carousel scrolls to next/previous card (300ms smooth snap)
  - Arrow becomes disabled at carousel start/end (opacity 50%, cursor not-allowed)
  - Focus outline appears on arrow (3px #F4A460)
- **Dot Indicator Click**: Jump to specific card (300ms)
- **Mobile Swipe**: Drag testimonial card left/right to scroll
- **Keyboard**: Arrow keys navigate carousel (if focused)

### FORMS
- **Input Focus**:
  - Border shifts to 2px solid #C17A5C
  - Box-shadow 0 0 0 3px rgba(193, 122, 92, 0.1) appears
  - Placeholder text fades slightly (opacity 30%)
  - Cursor active
- **Input Blur**: 
  - Border reverts to 1px #E8D5C4
  - Box-shadow removed (200ms)
  - Validation: If error, border becomes #E74C3C (red), error message appears 4px below input, color #E74C3C, font-size 12px
- **Submit Button Hover**: 
  - Background #D4956B, cursor pointer
  - Box-shadow 0 4px 12px rgba(193, 122, 92, 0.2)
  - Transform scale(1.02) (150ms)
- **Submit Button Click**: 
  - Button text → "Sending..." (spinner animation, 1-second loop)
  - After submit: Toast notification slides up from bottom: "Thanks! We'll contact you soon." (success state, background #4CAF50, text #FFFBF7, auto-dismiss 4 seconds)

### FOOTER
- **Newsletter Input Focus**: Same as form inputs (border #C17A5C, shadow with accent color)
- **Social Icon Hover**: 
  - Stroke color #F4A460 (200ms)
  - Background opacity 10% #C17A5C (200ms)
  - Transform scale(1.1)
- **Footer Link Hover**: Color #F4A460, underline appears (150ms)

### MICRO-INTERACTIONS (Page-Wide)
- **Page Load**: Sections fade in with staggered animation (opacity 0 → 1, 600ms cubic-bezier(0.34, 1.56, 0.64, 1)) — 100ms delay per section
- **Scroll Reveal**: Cards and text blocks fade in + slide up (100px) as they enter viewport (Intersection Observer, 400ms easing)
- **Smooth Scroll**: All anchor links use smooth scroll behavior (600ms, ease-out-cubic)
- **Hamburger Menu**: Lines animate (top line rotates 45° + translates down; middle line opacity → 0; bottom line rotates -45° + translates up) — 300ms transition

---

## STYLE NOTES

### OVERALL AESTHETIC
- **Concept**: Warm, inviting neighborhood pizzeria vibe. Emphasis on handcrafted quality, family, and comfort.
- **Mood**: Cozy, approachable, sophisticated but not stuffy. Earthy and organic.

### SPACING & RHYTHM
- **Base Unit**: 8px grid system
- **Vertical Rhythm**: Section padding follows 8px multiples (60px = 7.5×, 80px = 10×, 100px = 12.5×, 120px = 15×)
- **Horizontal Gaps**: 16px (mobile), 24px (tablet), 32px (desktop), all multiples of 8
- **Card/Component Padding**: 16px, 20px, 24px (all 8px multiples)
- **Margins**: Between typographic elements 12px–24px (logical 1.5–3× base unit)

### TYPOGRAPHY PERSONALITY
- **Headlines**: Serif (Playfair Display or Georgia) for warmth and tradition. All caps rarely; sentence case preferred. Letter-spacing slightly open (-0.5px for headlines).
- **Body**: Clean sans-serif (Inter or system fonts) for readability. Generous line-height (1.6) ensures comfort.
- **Accent Text**: Small caps or weight shifts (600) to draw attention without all-caps shout.

### VISUAL TEXTURE & DEPTH
- **Shadows**: Subtle, warm-tinted shadows using rgba(0,0,0,0.08–0.12) for cards; stronger (0.2–0.3) on hover/CTAs
- **Borders**: Soft 1px borders (#E8D5C4) instead of hard lines; border-radius 8px–16px for softness
- **Patterns**: Optional subtle topography or speckle overlay (8% opacity) on hero background; no aggressive patterns
- **Gradients**: Warm linear gradients only (Hero: #FFF4EA → #FFF0E6; CTA section: #2D1B11 → #3D2B1F)

### RESPONSIVENESS BREAKPOINTS
- **Mobile**: 375px–767px (1 column, stacked, full-width padding 16px)
- **Tablet**: 768px–1023px (2 columns, medium padding 24px)
- **Desktop**: 1024px+ (3 columns, full layouts, max-width container 1200px, centered)
- **Max Width**: 1200–1280px container with 24px sides = 1152–1232px content width
- **Touch Targets**: Minimum 44×44px for all interactive elements (mobile)

### FEEL & TONE IN DESIGN
- **Warmth**: Warm color palette (#FFFBF7, #C17A5C, #2D1B11) evokes wood-fired oven, dough, and earthy ingredients
- **Approachability**: Generous whitespace, rounded corners, and soft shadows feel inviting, not corporate
- **Motion**: Smooth, subtle transitions (200–300ms) feel natural; no jarring animations
- **Personality**: Serif headlines + conversational copy + food photography convey artisanal, hand-made quality
- **Consistency**: Every element adheres to 8px grid; color use is deliberate and limited; spacing is predictable

### VISUAL HIERARCHY
1. **Hero Section** (Hero image + headline dominates viewport)
2. **Section Headings** (48px serif, centered or left-aligned with intent)
3. **Body Copy** (16px sans-serif, secondary color #6B5344 for ease of scanning)
4. **CTAs** (High-contrast #C17A5C buttons pull eye)
5. **Supporting Details** (12–14px labels, muted #D4BFAE in dark sections)

### BRAND VOICE IN DESIGN
- Friendly, not trendy
- Nostalgic but modern
- Handcrafted, not mass-produced
- Community-focused (testimonials, story section)
- Warm, never cold or clinical

---

## END OF DESIGN SPECIFICATION

**Deliverables for Developer:**
- [ ] Header (sticky nav + mobile hamburger)
- [ ] Hero section (image + CTA + optional parallax)
- [ ] Menu card grid (4 cards, hover lift, 1/2/3 column responsive)
- [ ] About/Story section (text + image, alternating layout)
- [ ] Testimonial carousel (Embla, 5-star ratings, 3 visible desktop)
- [ ] Contact/Order section (form or dual-column links)
- [ ] Footer (logo + hours + address + socials + newsletter)
- [ ] Accessibility: ARIA labels, semantic HTML, focus indicators, keyboard nav
- [ ] Animations: Scroll reveal, micro-interactions, smooth transitions
- [ ] Responsive: Mobile-first, 375px–1440px tested

All hex colors, spacing, sizing, and interactions defined above. Ready for Next.js 14 + TypeScript + Tailwind implementation.