# Engineering Specification (Single-Page): prvc.app Website

## 1. Overview
A minimalist, high-performance single-page website designed to meet Apple 2026 App Store Review Guidelines. The primary goal is to provide a "one-stop" destination for Support, Privacy, and Feature verification via anchor-based navigation.

## 2. Architecture Decision
- **Framework:** **Astro** (for static generation and minimal JS).
- **Hosting:** **Vercel** or **Netlify** (for fast global delivery).
- **Navigation:** **Sticky Navigation** with anchor links (`#features`, `#privacy`, `#support`).
- **Smooth Scrolling:** Implemented via CSS (`scroll-behavior: smooth;`).

## 3. Page Structure (Vertical Flow)
1. **Header (Sticky):** Links to #Features, #Privacy, #Support.
2. **Hero:** App headline, subheadline, App Store Badge.
3. **Features Section (`#features`):** 4-6 feature cards with clear H2 headers.
4. **FAQ Section:** Based on official LinkedIn FAQ.
5. **Privacy Policy Section (`#privacy`):** Full, Apple-compliant policy.
6. **Support Section (`#support`):** Functional contact form and reply promise.
7. **Footer:** Copyright and social links.

## 4. Apple Compliance (Single-Page)
- **Direct Access:** The App Store Connect "Privacy Policy URL" must point to `https://prvc.app/#privacy`.
- **Direct Support:** The "Support URL" must point to `https://prvc.app/#support`.
- **Guideline 1.5 & 5.1:** Satisfied by the clear visibility and functionality of the respective sections on the single page.

## 5. Component Inventory
- **StickyNav:** Always visible at the top.
- **SectionContainer:** Standard padding and H2 styling for each section.
- **ContactForm:** Simple, stateless form for user support.
- **AppBadge:** Standard Apple App Store button.

## 6. Testing Checklist (Single-Page)
- [ ] Nav links correctly jump to the corresponding `#` section.
- [ ] Contact form is functional within the single-page flow.
- [ ] Privacy Policy is readable without clicking away to another page.
- [ ] Mobile navigation (Hamburger menu) also uses anchor links.
