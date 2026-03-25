SUMMARY: Design a warm, inviting landing page for a cozy pizza company that converts visitors into customers through storytelling, menu highlights, and frictionless ordering.

---

APPROACH:
- **Framework**: Next.js 14 (React) with TypeScript — fast builds, image optimization, server components
- **Styling**: Tailwind CSS + CSS custom properties for warm color palette consistency
- **Animations**: Framer Motion for subtle entrance animations and scroll triggers (no bloat)
- **Image handling**: Next.js Image component for responsive, optimized pizza photography
- **Forms**: React Hook Form + Zod for order/inquiry forms with client-side validation
- **Icons**: Heroicons or Feather Icons (lightweight, accessible SVGs)
- **Accessibility**: Built-in semantic HTML, ARIA labels, keyboard navigation throughout

Why this stack: Fast, accessible by default, excellent mobile performance, scales smoothly. No jQuery or heavy libraries.

---

REQUIREMENTS:

**Hero Section**
- Full-width hero with warm background (burnt orange, cream, or deep brown gradient)
- Headline + subheadline positioning (left-aligned, max 60 characters)
- High-quality hero image of signature pizza or cozy interior (right side, 50% width on desktop)
- Primary CTA button ("Order Now" or "Reserve Table") with hover state
- 8px grid alignment for all spacing and padding

**Navigation**
- Fixed or sticky header with logo, nav links, and CTA button
- Links: Home, Menu, About, Contact, Reviews
- Mobile hamburger menu with smooth slide-in animation
- Logo area sized for recognition (48px height minimum)

**Menu Preview Section**
- 3–4 featured pizza cards displayed in grid (1 col mobile, 2–3 col desktop)
- Each card: pizza image, name, 2–3 ingredient highlights, price
- Hover state: subtle lift (transform: translateY -4px), shadow increase
- "View Full Menu" CTA at section bottom

**About/Story Section**
- Warm, human-centered copy (100–150 words max) explaining brand values
- Small team photo or illustration of cozy pizza-making moment
- Icons for key attributes (🔥 handmade, 🌱 local ingredients, ❤️ family-owned)
- Left text, right image layout on desktop; stacked on mobile

**Customer Reviews Section**
- 3–5 testimonial cards with star ratings (5-star system)
- Reviewer name, location snippet, quote (50–80 words)
- Rotating or static carousel (if >5 reviews, use light carousel library like Embla)
- Cards in row with consistent spacing

**Contact/Order CTA Section**
- Two columns: "Order Online" (link to external ordering system) + "Call Us" (phone number as link)
- Alternatively: embedded form for reservations or inquiries
- Form fields: name, email, phone, message (optional)
- Form validation feedback inline, above submit button
- Submit button with loading state (spinner or text change)

**Footer**
- Dark background (contrast ratio 7:1 against light text)
- Sections: Hours, Address, Phone, Social links (Facebook, Instagram, etc.)
- Links to Privacy Policy, Terms
- Copyright notice
- Newsletter signup (optional) with single email field

**Responsive Breakpoints**
- Mobile: 375px+ (single column, stacked sections)
- Tablet: 768px+ (two-column layouts begin)
- Desktop: 1024px+ (full grid layouts, multi-column sections)
- Large: 1440px+ (max-width container at 1200px–1280px)

---

CONSTRAINTS:

**Performance**
- Lighthouse score target: 90+ (Core Web Vitals: LCP <2.5s, FID <100ms, CLS <0.1)
- All hero/above-fold images: WebP format with JPEG fallback, max 100KB
- No third-party trackers above the fold; defer analytics to after interaction

**Accessibility (WCAG AA)**
- Color contrast: all text on backgrounds must pass AA (4.5:1 for body, 3:1 for large text)
- Warm palette example: #8B4513 (saddle brown) text on #FFF8DC (cornsilk) = 8.2:1 ratio
- All buttons: minimum 44×44px touch target
- Form labels explicitly associated with inputs (htmlFor attribute)
- Image alt text: descriptive, not just "pizza"
- Focus states: visible 2px outline in accent color on all interactive elements

**Dependencies**
- Next.js 14+, React 18+
- Tailwind CSS 3.4+
- Framer Motion 10+ (for animations)
- React Hook Form 7.5+ (for forms)
- Zod 3.22+ (for validation)
- Embla Carousel or Swiper (if carousel needed — keep lightweight)

**Platform**
- Fully responsive web app (mobile-first design)
- Works on Safari 14+, Chrome, Firefox, Edge (last 2 versions)
- No Flash, no animated GIFs; use MP4 or WebM for video backgrounds (optional, with autoplay muted loop controls)

---

NOTES:

**Best Practices**
- Use semantic HTML5 tags: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Warm color palette psychology: oranges, warm browns, creams, rust tones build coziness and appetite appeal
- Imagery: use real pizza photos (not stock), show imperfections (char, bubbling cheese) — humanizes the product
- Micro-interactions: hover scale on cards (1.02–1.05), button transitions (200ms cubic-bezier), scroll fade-ins
- Typography: serif font for headlines (Georgia, Playfair Display) + sans-serif body (Inter, Poppins) for warmth + readability

**Edge Cases & Gotchas**
- Form submissions: confirm success state, don't just redirect (UX expectation)
- Pizza images: ensure consistent aspect ratio (16:9 or 4:3) to prevent layout shift
- Mobile menu: ensure z-index is high enough to overlay hero content; test close behavior on iOS
- Accessibility: don't hide focus states with `outline: none` — restyle instead
- Lazy loading: images below fold should load with `loading="lazy"` but ensure CLS doesn't spike
- Local phone numbers: use `<a href="tel:...">` for one-click calling on mobile
- Review section: if pulling from external API (Google, Yelp), cache reviews server-side to avoid API latency

**Brand Tone**
- Copy should feel warm, welcoming, unpretentious ("We make pizza the way Nonna taught us" vs. "Artisanal wood-fired cuisine")
- Avoid corporate jargon; speak like a local business
- Include subtle personality in microcopy (button hover text, form placeholders)