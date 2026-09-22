# Delta Children — Design System

A design system for **Delta Children**, a family-owned children's furniture and
juvenile-products brand (cribs, convertible & nursery sets, dressers/changing tables,
bassinets, high chairs, mattresses, strollers, wagons, and smart baby monitors). The
brand promise centers on **safe, healthier sleep** — GREENGUARD Gold certification,
JPMA-exceeding testing — paired with warm, aspirational nursery styling and accessible
price points. Voice is friendly, parent-to-parent, and reassuring.

This project recreates the brand's storefront foundations: the blue-led color system,
the Luxenta + Poppins type pairing, reusable commerce UI components, and full
recreations of the **Homepage** and **Product Detail Page**.

## Sources
- **Figma:** "Delta Children_ Claude.fig" — pages *Homepage-and-PDP* (Homepage,
  Product Page, Brand Colors, Fonts). Mounted as a read-only VFS for this build.
- **Fonts:** `Luxenta-Regular.otf` supplied by the brand (display face). Poppins and
  Hanken Grotesk pulled from Google Fonts.
- Brand rule provided with the file: *type sizes follow a proportion increasing in 4*.

> The reader may not have access to the Figma file; everything needed is captured here
> and in the token CSS, components, and UI kits.

---

## CONTENT FUNDAMENTALS

**Voice.** Warm, encouraging, parent-to-parent. The brand speaks *to* the shopper
("**your** baby", "**your** dream nursery") and about itself as a family ("**We** Are
Family", "**We're** obsessed with safety"). Confident and benefit-led, never clinical.

**Tone.** Upbeat and reassuring. Headlines frequently end in an exclamation point
("Build Your Dream Nursery & Save!"). Safety and trust copy is calm and factual
(numbers, certifications) to earn confidence.

**Casing.**
- *Section titles (Luxenta):* Title Case — "Find the Perfect Fit for Every Stage of
  Childhood", "What's Trending This Month".
- *Eyebrows (Poppins bold):* Title Case — "Mix & Match Your Favorites", "Shop by Category".
- *Micro labels / category tags:* lowercase or UPPERCASE with wide letter-spacing —
  "nursery sets", "BUNDLE & SAVE", "NEW ARRIVAL".
- *Promo strip:* sentence-ish with emphasis caps — "Winter Sale: 15% Off Sitewide with
  Code WINTER15".

**Person.** Second person to the customer ("you / your"), first-person plural for the
brand ("we / our"). No corporate "the company".

**Numbers & proof.** Lean on concrete proof: "GREENGUARD Gold Certified", "tested
against 10,000+ chemicals", "50 years", "1 in 2 babies", star ratings + review counts,
"Verified Customer". Prices show a struck-through compare-at + a savings badge.

**Emoji.** Not used in copy. The only "emoji-like" mark is the **♥ heart** inside the
logo wordmark — a brand device, not punctuation.

**Examples (verbatim & in-voice):**
- "Build Your Dream Nursery & Save!"
- "Healthier Sleep Starts Here"
- "The only chair you'll ever need"
- "Real Parents. Real Reviews."
- "Sign Up & Get a Surprise Offer"
- "#DeltaChildren — tag us to share your nursery"

---

## VISUAL FOUNDATIONS

**Color.** The system is built on **one chromatic blue ramp** (`lightblue-10 → 100`),
not a multi-hue palette. `lightblue-80` (#3575CA) is the action base; `lightblue-90`
is its border/hover; `lightblue-100` (#2B5EA1) is the heading blue used for nearly all
section titles and eyebrows; `lightblue-ink` (#1A3A6C) is reserved for deep nursery
copy. A full neutral gray ramp (white → #1E1E1E) carries text and surfaces. A single
**seasonal promo green pair** (olive #5C664D bg / pale #EAECDE text) is used only for
the sale strip banner. Sale price accents use a warm red. Backgrounds alternate between
white and a very pale blue tint (`lightblue-10`) to separate sections.

**Type.** Two families. **Luxenta** (brand display, geometric, friendly) sets the logo,
hero lockups, and every section title — almost always in heading blue, Title Case,
~1.1–1.2 line height. **Poppins** carries all body, UI, labels and buttons; eyebrows
are Poppins **Bold 14**, buttons Poppins **SemiBold 16**, micro labels Poppins Medium 10–12
with 0.1em tracking, UPPERCASE. Sizes step in **multiples of 4**. (Hanken Grotesk
appears in a few utility spots and is included as a fallback/accent.)

**Spacing & layout.** 4px base unit; spacing scale climbs in fours. Desktop content sits
in a **1360px** max-width frame with 40px gutters. Sections are generous (≈56–64px
vertical padding). Grids are the backbone — 3 & 4-up product/category grids with 16–20px
gaps.

**Corner radius.** **8px is the brand default** for buttons, cards, inputs, tiles and
images. 2–4px for hairline chips; pills (999px) for color swatches, round carousel
buttons, the search field and tags.

**Cards.** White surface, 8px radius, a 1px hairline inset border (`border-hairline`)
or a soft ambient shadow (`shadow-card`). On hover, content cards lift slightly
(translateY -2px) and gain `shadow-hover`. Category/hero image cards crop to a fixed
aspect ratio with the info band beneath (tinted) or a bottom gradient scrim for overlaid
text.

**Shadows / elevation.** Low and soft. A layered ambient stack (`shadow-ambient`) sits
under floating UI. The **primary button** is the signature: a faint **blue glow**
(`rgba(0,106,255,0.2)`, 15px blur) plus the ambient stack and a 1px inner blue border —
a soft, lifted, "tappable" look.

**Backgrounds & imagery.** No heavy gradients or textures as page backgrounds — just
white and pale-blue tints. Imagery is the star: warm, naturally-lit **nursery lifestyle**
photography (light woods, creams, soft blues, real parents and babies), clean product
shots on contrasty or neutral backdrops, and casual **vertical UGC/influencer** clips for
social proof. Overall image vibe is **warm and soft**, never cold or high-contrast B&W.

**Borders.** 1px hairlines for dividers and card outlines (`border-hairline` /
`border-subtle`); the **secondary button** uses a 2px blue inset outline. Inputs use a
1px gray border that becomes a 2px blue ring on focus.

**Buttons & states.**
- *Primary* — solid blue, white bold text, blue glow. Hover darkens to `lightblue-90`.
- *Secondary* — white with a 2px blue outline; hover fills with pale-blue tint.
- *Tertiary* — blue text link; hover underlines.
- *Ghost* — quiet neutral; hover gets a faint gray wash.
- *Press* — all buttons nudge down 1px (`translateY(1px)`); no scale-bounce.

**Motion.** Restrained and functional. 120–320ms with a standard ease
(`cubic-bezier(.4,0,.2,1)`) for hovers, accordion open/close (animated grid rows), and
toasts (ease-out, slide-up + fade). Image cards do a subtle 1.04 zoom on hover. No
infinite/decorative loops.

**Transparency & blur.** Used sparingly — a dark bottom gradient scrim over hero imagery
so white text stays legible. No glassmorphism.

---

## ICONOGRAPHY

The brand's interface uses **Heroicons (Outline)** — the Figma layers reference
`HeroiconsOutline*` (e.g. X-Circle, SpeakerXMark) for UI glyphs, plus a small set of
custom marks (the GREENGUARD shield/leaf badge, the logo heart, star ratings).

- **Style:** thin **outline**, ~2px stroke, rounded caps & joins, 24px grid. Single-color,
  usually `darkest-gray` for neutral UI or `action` blue for interactive/affordance icons.
- **In this system:** icons are drawn inline as stroke SVGs in that same Heroicons-outline
  manner (search, cart, account, info, chevron, check, heart) inside `StoreChrome.jsx` and
  the components. For production, install **[Heroicons](https://heroicons.com)** (outline
  set) — it matches 1:1. *(Substitution flagged: we hand-built the few glyphs the kit
  needs in Heroicons-outline style rather than bundling the full icon library.)*
- **Stars:** custom blue star (`rating-star` = action blue), filled for the score and
  outlined for the remainder — see the `Rating` component.
- **Logo heart:** the ♥ between DELTA and CHILDREN is a filled vector in brand blue.
- **Emoji / unicode as icons:** not used.

Assets live in `/assets` (`/assets/images` photography, `/assets/fonts` the Luxenta
binary). Real partner/press trademarks are intentionally not reproduced.

---

## INDEX / MANIFEST

**Root**
- `styles.css` — global entry point (imports only). Consumers link this.
- `readme.md` — this guide.
- `SKILL.md` — Agent-Skills wrapper.

**`tokens/`** — `fonts.css` (Luxenta @font-face + Google imports), `colors.css`,
`typography.css`, `spacing.css` (spacing, radii, shadows, motion). All `@import`ed by
`styles.css`.

**`guidelines/`** — foundation specimen cards (Design System tab):
color (primary ramp, neutrals, semantic & promo), type (Luxenta display, Poppins body,
+4 size scale, section-header pattern), spacing (scale, radii & elevation).

**`components/`** — reusable primitives (namespace `DeltaChildrenDesignSystem_6fc118`):
- `core/` — **Button, IconButton, Badge, Tag, Rating, SectionHeader, Pagination**
- `forms/` — **Input, QuantityStepper, ColorSwatch, Checkbox, Radio + RadioGroup**
- `feedback/` — **Accordion, Tooltip, Modal, Spinner, Skeleton**
- `commerce/` — **ProductCard, CategoryCard**
- `brand/` — **Logo**
Each directory has one or more `@dsCard` HTML thumbnails; each component has `.d.ts` + `.prompt.md`.

*Selection controls* (Checkbox, Radio) are 20px marks with a 2px brand-blue ring;
checked checkboxes fill blue with a white check, radios show a 10px blue dot.
*Tag* is the pale-blue (`lightblue-20`) filter chip with a bold blue label and an
optional dismiss ✕. *Pagination* tiles sit in 44px touch targets (32px visible, 4px
radius); the current page fills blue. *Tooltip* is a slate (`darker-gray`) bubble with
a beak, shown on hover/focus. *Modal* is a 24px-radius card on a deep-blue scrim,
closing on Esc or scrim click. *Spinner* / *Skeleton* are the loading primitives — a
brand-blue ring and shimmer placeholders, both honoring `prefers-reduced-motion`.

**`ui_kits/storefront/`** — full storefront recreation: `index.html` (interactive),
`homepage.html` & `product.html` (starting points), plus `StoreChrome.jsx`,
`Homepage.jsx`, `ProductPage.jsx`. See its `README.md`.

**`assets/`** — `fonts/Luxenta-Regular.otf`; `images/` brand photography & UGC.
