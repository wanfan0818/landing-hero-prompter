# Prompt Templates Library

## Template A: Hero Brief

```markdown
Design Prompt: Create a [mood] hero section for "[Brand]" - [product summary].

Brand Identity:
Use a palette built from [primary colors]. Typography should use [font pairing]. The overall tone should feel [tone words].

Visual Thesis:
[one sentence describing the hero as an image system, not just a UI block]

Composition Rules:
- [what dominates the frame]
- [where the negative space lives]
- [how the text block is anchored]
- [what should feel restrained vs emphasized]

Material Hierarchy:
- Primary: [dominant surface language]
- Secondary: [supporting material or emphasis layer]
- Tertiary: [sparingly used glow / chrome / blur / particles / accent]

Layout & Positioning:
- Header: [logo placement, navigation style, CTA placement]
- Main Hero: [left-aligned / centered / split], positioned [upper third / center / bottom-weighted]
- Supporting Element: [stats / consultation card / partner bar / dashboard preview / none]

Key Design Elements:
- Background: [MP4 / HLS / image / gradient / texture] with [overlay behavior]
- Buttons: [rounded / clipped / glass / solid], with [accent color and hover behavior]
- Surface Treatments: [glass / shine / inner shadow / border treatment / none]
- Scale: desktop headline around [size], mobile headline around [size]

Technical Details:
- Stack: [framework and CSS stack]
- Fonts: [exact font families]
- Icons: [library or named icons]
- Responsiveness: [desktop and mobile padding/scaling rules]
- Motion: [fade-up / blur reveal / stagger / none]
```

## Template B: Page Rebuild

```markdown
Build a single-page landing page for [brand/product] using [stack].

VISUAL THESIS
- [what the page feels like in one sentence]

COMPOSITION RULES
- [hero composition]
- [negative space strategy]
- [type vs media relationship]
- [how asymmetry / symmetry should be handled]

FONTS & DESIGN SYSTEM
- [fonts and token rules]

MATERIAL HIERARCHY
- Primary: [dominant shell / field / material]
- Secondary: [repeated emphasis treatment]
- Tertiary: [rare accent effect]

SIGNATURE MATERIALS / EFFECTS
- [glass / clipped corners / blur text / video fades / repeated materials]

SECTION RHYTHM
- Hero: [attraction]
- Mid-page explanation: [clarity]
- Immersive block: [emotional proof]
- Metrics / specs: [authority]
- CTA: [closure]

SECTION 1 - [NAME]
- [layout]
- [content hierarchy]
- [media behavior]
- [motion behavior]

SECTION 2 - [NAME]
- [layout]
- [content hierarchy]
- [media behavior]
- [motion behavior]

[Continue section-by-section as needed]

DEPENDENCIES
- [package list]

KEY PATTERNS
- [repeated badge rule]
- [repeated heading rule]
- [repeated card rule]
- [repeated video rule]
```

## Template C: Page Rebuild With Strong Design System

```markdown
Build a single-page landing page for [brand/product] using [stack].

VISUAL THESIS
- [campaign-grade one-line visual thesis]

COMPOSITION RULES
- [dominant force in hero]
- [negative space and alignment logic]
- [how the product / video / text should share the frame]

MATERIAL HIERARCHY
- Primary: [dominant shell / field]
- Secondary: [glass / reflection / metallic / card treatment]
- Tertiary: [glow / particles / annotations / motion accents]

GLOBAL DESIGN SYSTEM
- Fonts: [exact families and weights]
- CSS Variables: [list exact root tokens]
- Tailwind Extensions: [fontFamily / colors / keyframes / animations]
- Utility Classes: [liquid-glass / clipped-corner / marquee / etc.]
- Button Variants: [hero / heroSecondary / outline / etc.]

SECTION 1 - HERO
- [exact media and overlay treatment]
- [navbar structure]
- [headline / subheadline / CTA]
- [bottom strip / partner marquee / widget]

[Continue as needed]

KEY DEPENDENCIES
- [package list]

PAGE STRUCTURE
- [top-level component order]
```

## Template D: Hardware Campaign Page

```markdown
Build a single-page landing page for [brand/product] using [stack].

VISUAL THESIS
- [premium hardware reveal in one sentence]

COMPOSITION RULES
- [hero object dominates the frame]
- [negative space strategy]
- [media should feel cropped / oversized / staged]
- [avoid generic SaaS card rhythm]

MATERIAL HIERARCHY
- Primary: [matte shell / optical darkness / industrial surface]
- Secondary: [lens reflections / smoked glass / restrained translucent layers]
- Tertiary: [rare accent energy used only for intelligence or optical glow]

TYPOGRAPHY RULES
- [headline behavior]
- [body behavior]
- [technical label behavior]

SECTION RHYTHM
- Object Reveal
- Precision Strip
- Immersive Proof
- Capability Modes
- Materials / Engineering Detail
- Reserve / CTA

SECTION 1 - OBJECT REVEAL
- [hero object staging]
- [headline / subheadline / CTA]
- [technical notation or restrained support details]

SECTION 2 - PRECISION STRIP
- [compressed spec band or instrumentation layout]

SECTION 3 - IMMERSIVE PROOF
- [full-bleed contextual media]
- [sparse AR / UI annotation treatment if needed]

SECTION 4 - CAPABILITY MODES
- [alternating vignettes instead of generic cards]

SECTION 5 - MATERIALS / ENGINEERING DETAIL
- [macro crops / close-up materials / exploded technical cues]

SECTION 6 - RESERVE / CTA
- [sparse premium closing block]

KEY CONSTRAINTS
- [what the page must not become]
```
