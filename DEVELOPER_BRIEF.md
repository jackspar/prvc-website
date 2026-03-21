# Developer Brief: prvc.app Website

**Client:** Combinatorial Security Holdings Inc.
**Contact:** support@prvc.app
**Last Updated:** March 20, 2026

---

## What You're Building

A single-page marketing and compliance website for **prvc.app** — an identity-free, P2P encrypted messaging app for iOS. The site must be live at `prvc.app` before the app can be submitted to the Apple App Store.

**This is not a marketing exercise.** The website is an Apple App Store compliance instrument. Every section exists to satisfy a specific Apple Review Guideline. Do not remove or rename sections without checking the compliance checklist first.

---

## Stack

| Decision | Choice | Reason |
| :--- | :--- | :--- |
| Framework | **Astro** | Static generation, minimal JS, fast |
| Styling | **Vanilla CSS** | No framework dependencies |
| Hosting | **Vercel or Netlify** | Free tier, global CDN, auto-deploy from git |
| Domain | `prvc.app` | Already registered — client to configure DNS |

---

## Files in This Repo

| File | Purpose |
| :--- | :--- |
| `docs/WEBSITE_CONTENT.md` | **Start here.** All copy, section by section, verbatim. Build from this. |
| `docs/ENGINEERING_SPEC.md` | Architecture decisions, component inventory, Apple compliance anchors |
| `docs/APPLE_SUBMISSION_CHECKLIST.md` | Compliance checklist — verify each item before handoff |
| `public/prvc-logo.jpg` | Logo asset |
| `public/app-icon-placeholder.svg` | App icon placeholder — replace with final 1024×1024 PNG |
| `preview.html` | Visual reference — open in browser to see the target design |

---

## Page Structure

Single page. All navigation is anchor-based. **Do not change anchor IDs** — Apple has these URLs on file.

| Section | Anchor | Apple Guideline |
| :--- | :--- | :--- |
| Sticky Nav | — | 1.5, 5.1 |
| Hero | `#hero` | 2.3.1 |
| Why prvc.app? | `#why-prvc` | 2.3.1 |
| Features | `#features` | 1.2, 5.1.1v |
| FAQ | `#faq` | 1.2, 5.1.1v |
| Privacy Policy | `#privacy` | 5.1, 5.1.2(i) |
| Terms of Service | `#terms` | EULA |
| Support | `#support` | 1.5 |
| Footer | — | Legal |

**Critical URLs Apple will test:**
- `https://prvc.app/#privacy` — Privacy Policy URL in App Store Connect
- `https://prvc.app/#support` — Support URL in App Store Connect

---

## Design Reference

Open `preview.html` in any browser for the visual target. Dark theme, electric cyan accent (`#00D4FF`), -apple-system font stack.

---

## Prohibited Language

Do not introduce any of the following — they are Apple rejection triggers:

- "Login" / "Log in" (use "Connect" or "Initiate")
- "Anonymous" as a claim (use "Identity-Free")
- "Unhackable", "100% secure", "Military grade", "Unbreakable"
- Any mention of AI or third-party ML models

---

## Open Items (Pending Client)

These assets are not yet available — use placeholders until received:

- [ ] Final App Store icon (1024×1024 PNG, no alpha, no rounded corners)
- [ ] App Store badge URL (once app is live)
- [ ] Twitter/X handle for footer
- [ ] High-fidelity app screenshots

---

## Handoff Checklist

Before going live, verify:

- [ ] All anchor links resolve correctly
- [ ] `support@prvc.app` mailto link works
- [ ] Site renders correctly on iPhone Safari (primary Apple reviewer device)
- [ ] Lighthouse score: 90+ Performance, 100 Accessibility
- [ ] HTTPS live on `prvc.app`
- [ ] All placeholder text removed
