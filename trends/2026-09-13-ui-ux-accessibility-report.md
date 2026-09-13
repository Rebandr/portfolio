# UI/UX & Accessibility Weekly Scan — 2026-09-13

A weekly dual-focus digest: cutting-edge interface trends alongside accessibility, compatibility, and public-sector compliance developments. Measurements use the metric system throughout.

---

## Part 1: Cutting-Edge UI/UX & Component Trends

### Design system moves
- **Apple HIG / Liquid Glass** — Apple's Human Interface Guidelines continue refining guidance for the "Liquid Glass" material introduced with iOS 26. The core principle is "hierarchy through depth": interface importance is communicated through layered translucency, refraction, and specular highlights that react to motion, rather than through contrast or size alone. The Materials section of the HIG has been expanded with concrete do/don't guidance for when to apply glass surfaces to navigation bars, controls, and sheets. [Pixel Envy](https://pxlnv.com/linklog/hig-liquid-glass/), [Wikipedia: Liquid Glass](https://en.wikipedia.org/wiki/Liquid_Glass)
- **Google Material 3 Expressive** — Google's rollout of Material 3 Expressive is now well underway across its own product suite (Google Drive, Google Tasks widgets, Chrome for Android Settings). The system emphasizes "sensory design": springy, physics-based motion, brighter and more customizable color, tactile surface depth, and an expanded Material Shapes Library that has grown to 35 shapes with shape-morphing support in both Figma and Jetpack Compose. Material You is also gaining fully custom user-picked accent colors rather than only wallpaper-derived palettes. [9to5Google](https://9to5google.com/guides/material-3-expressive/), [Supercharge Design](https://supercharge.design/blog/material-3-expressive)
- **Shopify Polaris & Vercel Geist** — Both remain stable, actively maintained systems this cycle (component libraries, tokens, and API-driven documentation); no major version announcements surfaced this week, but they remain useful reference points for admin-dashboard and developer-tool patterns respectively. [Shopify Polaris update](https://www.shopify.com/partners/blog/polaris-update), [Geist Design System](https://designsystems.surf/design-systems/vercel)

### Component & interaction patterns seeing active adoption
- **Calmer, functional micro-interactions** — Heavy, decorative animation is fading in favor of lighter, purposeful feedback (state changes, subtle haptic-style cues) that doesn't cost performance. Motion is increasingly held to a stricter "does this aid understanding" bar rather than being purely decorative.
- **Bottom-anchored mobile navigation** — Bottom tab bars and gesture-driven navigation (swipe, pinch) continue displacing top tab bars in consumer mobile apps, reducing on-screen chrome in favor of thumb-zone reachability.
- **Larger, thumb-zone touch targets** — Minimum touch target sizes are solidifying at roughly **1.1 cm × 1.1 cm** (44×44 px, iOS) and **1.27 cm** (48 dp, Android), with single-thumb flows prioritized for primary actions and larger hit areas recommended for outdoor/bright-light use.
- **Data-dense dashboards, still simplified** — Data-table and dashboard patterns continue trending toward progressive disclosure (summary first, drill-down on demand) paired with heavier reliance on real usage analytics (drop-off points, dead clicks) to justify layout decisions over pure visual opinion.
- **AI-assisted prototyping in the design process** — NN/g highlights that AI tooling now makes it practical to build fully interactive, high-fidelity prototypes of complex interfaces early, shifting usability testing earlier in the design cycle instead of validating static mockups. [NN/g Articles](https://www.nngroup.com/articles/)

---

## Part 2: Accessibility, Compatibility & Public Sector Compliance

### Regulatory: European Accessibility Act (EAA)
- The EAA has been enforceable since **28 June 2025**, and 2026 marks its first full year of active supervision. Enforcement is uneven across member states but accelerating: the first lawsuits were filed in France in November 2025, and the Netherlands and other states are ramping up enforcement activity through 2026. Penalties vary sharply by country — from roughly **€60,000 in Ireland** up to **≈€900,000 in Sweden** — and apply to any business (including non-EU companies) offering covered digital products/services to EU consumers. Practical takeaway: EN 301 549 / WCAG 2.1 AA conformance is no longer optional due-diligence, it is an active enforcement target. [Level Access: EAA in 2026](https://www.levelaccess.com/blog/eaa-compliance-in-2026-how-enforcement-has-evolved-and-what-to-expect-next/)

### WCAG & color contrast
- **WCAG 2.2** remains the current, enforceable standard; **4.5:1** contrast for normal text and **3:1** for large text and meaningful non-text elements (icons, focus indicators) are still the baseline AA targets.
- **WCAG 3.0** is still a Working Draft — it introduces a Bronze/Silver/Gold scoring model, the **APCA** perceptual contrast algorithm (replacing the current ratio-based formula), and expanded cognitive-accessibility guidance. The final contrast algorithm for WCAG 3 is still undecided, but teams doing a major design-system refresh in 2026 are advised to start testing against APCA now as a forward-looking check alongside WCAG 2.2 ratios. [Adrian Roselli: WCAG3 Contrast as of April 2026](https://adrianroselli.com/2026/04/wcag3-contrast-as-of-april-2026.html)
- Color contrast remains the single most common accessibility failure on the web — the WebAIM Million study found contrast issues on **83.6%** of scanned homepages in 2025, underscoring that this is a solved-in-theory, unsolved-in-practice problem.

### Public sector benchmarks: Digg (Webbriktlinjer) & Funka
- **Digg / Webbriktlinjer** — Digg's guidelines portal continues to serve as the reference implementation of DOS-lagen (Sweden's law on accessibility of digital public services): public bodies search Webbriktlinjer for the specific guidance items they must meet. Digg's own accessibility statement is transparent about known partial non-conformance on digg.se itself and provides a reporting channel for users who find unaddressed issues — a useful model for how a public-sector site should self-report accessibility debt. [Digg Webbriktlinjer](https://www.digg.se/webbriktlinjer/), [Digg Tillgänglighet](https://www.digg.se/webbriktlinjer/tillganglighet)
- **Funka Inkluderingsbarometer** — Funka's Inclusion Barometer, its recurring public-sector accessibility benchmark, found that only **17%** of tested public sector websites passed the selected accessibility tests — a stark reminder that legal obligation and practical conformance remain far apart even in a market (Sweden) with some of the strictest enforcement penalties in the EU. [Funka Nu AB / Cision](https://news.cision.com/se/funka-nu-ab/r/funkas-inkluderingsbarometer-avslojar-bristande-digital-tillganglighet-inom-offentlig-sektor,c3839670)

### Inclusive design: beyond WCAG checkboxes
- **Neuroinclusive design** is gaining sustained traction as a distinct discipline from strict WCAG conformance. NN/g's coverage (early September 2026) frames it around five practical levers: **simplicity, clarity, control, support, and co-creation** — designing for users under executive-function, communication, or sensory load in a way that improves usability for everyone, not just neurodivergent users. This pairs well with "design för alla" (design for all) framing used by Nordic public-sector guidance. [NN/g Articles](https://www.nngroup.com/articles/)

---

## Actionable Takeaways (Top 3)

1. **Treat APCA/WCAG 3 contrast testing as a parallel check, not a replacement, in any 2026 design-system refresh.** Keep shipping to WCAG 2.2 AA ratios (4.5:1 / 3:1) since that's what's legally enforced today, but run new color tokens through APCA as well so the system doesn't need a rebuild when WCAG 3 formalizes — especially relevant if adopting depth/translucency-heavy patterns like Liquid Glass, where a surface's effective contrast shifts with what's behind it.
2. **If your product or clients sell into the EU, audit EAA/EN 301 549 conformance now, not after a complaint.** Enforcement moved from theoretical to active in 2026 (first lawsuits, market-surveillance inspections, fines up to ~€900,000 in Sweden). Use Digg's Webbriktlinjer as a concrete checklist and Funka's Inclusion Barometer methodology as a benchmark — the 17% public-sector pass rate shows checkbox compliance alone isn't enough; test with real assistive-technology and keyboard-only flows.
3. **When adopting trendy motion/glass/expressive visual systems (Liquid Glass, Material 3 Expressive), gate every new pattern through touch-target size (≥1.1 cm) and reduced-motion/neuroinclusive review before shipping.** Springy animations and translucent depth cues are visually current, but they must degrade gracefully for `prefers-reduced-motion`, remain legible for low-vision users, and not rely on motion or transparency alone to convey hierarchy — pair them with the simplicity/clarity/control principles from neuroinclusive design so visual trend-chasing doesn't regress compliance.
