---
name: landing-hero-prompter
description: High-fidelity landing page prompt generator. Produces design-director style prompts for React + Tailwind hero sections and full landing pages from product descriptions or visual references, with precise layout, typography, motion, glass, and video guidance.
---

# Landing Hero Prompter

Generate a production-grade prompt for an AI coding assistant to build a landing page hero section or, when the reference clearly demands it, a full single-page landing page.

The output should feel like a strong design brief first, and a technical specification second.
Do not default to a giant component checklist unless the user explicitly asks for implementation detail or provides a dense full-page reference that clearly requires reconstruction.

## Core Positioning

This skill exists to create prompts that are:

1. Visually opinionated, not generic.
2. Precise enough to implement without guesswork.
3. Written in the tone of a design director briefing an engineer.
4. Compatible with React + Tailwind CSS workflows.
5. Grounded in exact values for color, spacing, typography, and motion.

## Non-Negotiables

Always follow these rules:

1. Start with a strong `Design Prompt:` style opening, not with package installation.
2. Lead with brand identity, layout intent, visual hierarchy, and signature effects.
3. Keep the prompt compact and high-signal. Favor direction over bloated scaffolding.
4. Use precise values when they matter: hex/HSL, px, blur radius, opacity, clip-path cuts, font sizes, spacing.
5. Preserve the user's requested visual character. Do not sand it down into safe SaaS UI.
6. Only include code snippets for distinctive implementation details such as liquid glass, clipped corners, video, masks, or motion patterns.
7. If a screenshot/reference image is provided, match its composition, density, and mood before adding your own enhancements.
8. Avoid placeholder copy. Generate real headline, subheadline, CTA, and nav copy.

## Output Philosophy

The current skill should optimize for prompts like this:

- Short opening directive
- Brand Identity
- Layout & Positioning
- Key Design Elements
- Technical Details
- Optional Implementation Notes

It should not optimize for this by default:

- Huge `Technical Setup`
- Long dependency tables
- Full JSX skeletons for every block
- Repetitive "Key Design Decisions" sections that restate obvious things

If the user explicitly asks for implementation-heavy output, or provides a detailed full-page reference, then expand into section specs after the design brief.

## Output Modes

Choose one of these modes deliberately:

### Mode A: `hero-brief`

Use when:

- the user asks for a hero section
- the user wants a concise prompt
- the user gives a style direction but not a full page blueprint

Output shape:

- `Design Prompt`
- `Brand Identity`
- `Layout & Positioning`
- `Key Design Elements`
- `Technical Details`
- optional `Implementation Notes`

### Mode B: `page-rebuild`

Use when:

- the user provides a detailed multi-section reference
- the prompt includes repeated `SECTION 1`, `SECTION 2`, `SECTION 3` style breakdowns
- the user wants a page recreated, not just a hero inspired by a style
- there are required custom primitives like `BlurText`, HLS backgrounds, liquid-glass variants, alternating feature rows, testimonial cards, stats blocks, or CTA footer logic

Output shape:

- short opening directive
- `FONTS & DESIGN SYSTEM`
- `SIGNATURE MATERIALS / EFFECTS`
- `SECTION-BY-SECTION SPEC`
- `DEPENDENCIES`
- `KEY PATTERNS`
- optional `PROMPT TO RECREATE LANDING PAGE`

In `page-rebuild` mode, preserving structure is more important than brevity.

## Resources

Use these files as needed:

- `resources/design_tokens.md`
- `resources/layout_composition_rules.md`
- `resources/hardware_campaign_rules.md`
- `resources/liquid_glass.md`
- `resources/animation_patterns.md`
- `resources/video_patterns.md`
- `resources/component_templates.md`
- `resources/visual_analysis_guide.md`
- `resources/copywriting_formulas.md`
- `resources/prompt_templates.md`

Examples:

- `examples/dark_saas.md`
- `examples/glass_creative.md`
- `examples/light_fintech.md`
- `examples/cinematic_dark_logistics.md`
- `examples/apple_glass_full_page.md`
- `examples/editorial_impact_full_page.md`
- `examples/green_glass_saas_full_page.md`
- `examples/hardware_campaign.md`

## Workflow

### Phase 0: Gather Inputs

Collect these if available:

1. Brand or product name
2. One-line product description
3. Industry / audience
4. Desired tone or style
5. Video URL, if any
6. Reference screenshot or site, if any
7. Required framework or libraries
8. Whether this is hero-only or full-page

Use reasonable assumptions if the user is missing details.

### Phase 0.5: Visual Reference Analysis

Only do this if the user provides a visual reference.

Extract:

1. Overall light/dark balance
2. Composition: centered, upper-third, split, editorial, asymmetrical
3. Typography personality: geometric, editorial, industrial, soft, brutal, premium
4. Density and scale: spacious, compact, oversized, restrained
5. Signature treatments: glass, shine, clipped corners, strokes, glow, grid, noise, chrome, HUD
6. Motion cues: calm fade, cinematic reveal, hover aggression, parallax, marquee

Then turn that into a compact parameter card that overrides generic defaults.

Also classify the request:

- `hero-brief`
- `page-rebuild`

### Phase 1: Choose the Design Direction

Infer a design system from the product and reference:

- AI / SaaS / dev tools: dark premium, dark tech, clean editorial, or glass-heavy dark SaaS when the reference includes translucent surfaces and vivid accent color
- Finance / enterprise: refined light or restrained dark premium
- Healthcare / wellness: clean light or cool-accent minimal
- Logistics / industrial / transport: dark industrial, compact, directional, high-contrast
- Sustainability / climate / ESG / impact consulting: editorial dark, restrained premium, trustworthy, often supported by steel-to-gold accent gradients
- Creative / agency / fashion: editorial, glass, asymmetry, stronger art direction

Pick one primary style and at most two overlays, such as:

- `dark-premium + industrial-red`
- `clean-light + cool-accent`
- `editorial-minimal + liquid-glass`
- `editorial-dark + impact-gradient`
- `dark-premium + climate-editorial`
- `dark-saas + liquid-glass + green-accent`

### Phase 1.5: Route to the Right Pattern

Use this routing table before writing the final prompt.

| If the input feels like... | Use output mode | Preferred style family | Closest example |
|---|---|---|---|
| single hero request, no dense section breakdown | `hero-brief` | choose from product category | `examples/dark_saas.md` or `examples/light_fintech.md` |
| dark analytics / dashboard SaaS hero | `hero-brief` | `dark-premium` | `examples/dark_saas.md` |
| light fintech / payment / infrastructure hero | `hero-brief` | `clean-light + warm-accent` | `examples/light_fintech.md` |
| industrial / transport / logistics page with sharp geometry | `page-rebuild` | `dark-industrial + directional` | `examples/cinematic_dark_logistics.md` |
| dark glass agency / Apple-like motion / cinematic video page | `page-rebuild` | `liquid-glass + black-shell` | `examples/apple_glass_full_page.md` |
| AR / XR / wearable hardware launch page | `page-rebuild` | `hardware-campaign + optical-dark` | `examples/hardware_campaign.md` |
| editorial climate / sustainability / ESG / regeneration brand | `page-rebuild` | `editorial-dark + impact-gradient` | `examples/editorial_impact_full_page.md` |
| revenue platform / sales ops / growth SaaS with translucent glass and vivid green CTA | `page-rebuild` | `dark-saas + liquid-glass + green-accent` | `examples/green_glass_saas_full_page.md` |
| creative platform with dark cinematic glass and serif-led typography | `page-rebuild` | `creative-glass + display-serif` | `examples/glass_creative.md` |

When multiple rows seem plausible, choose based on these tie-breakers:

1. Match page structure first.
2. Match recurring materials second.
3. Match typography personality third.
4. Match accent color system fourth.

If the user provides a strong reference, the reference wins over category defaults.

### Phase 1.6: Decide Output Density

Use this quick density rule:

- If the user gives a short brief, produce a strong concise prompt.
- If the user gives section-by-section content, preserve section-by-section density.
- If the user names specific CSS classes, animations, HLS/MP4 behavior, or component names, keep them explicit.
- If the user gives a screenshot only, infer structure but keep the prompt shorter unless they clearly want a rebuild.

### Phase 2: Set The Composition Layer

Before generating copy or section specs, decide whether the prompt needs an explicit composition layer.

Load `resources/layout_composition_rules.md` when the request implies:

- premium or luxury presentation
- editorial or campaign-like art direction
- futuristic hardware or product-as-object treatment
- unusually strong reference imagery
- a page that should feel sparse, cinematic, asymmetrical, or brand-led instead of SaaS-modular

If it applies, establish these four items before the section list:

1. `Visual Thesis`
2. `Composition Rules`
3. `Material Hierarchy`
4. `Section Rhythm` for full pages, or an abbreviated rhythm statement for hero-only prompts

Load `resources/hardware_campaign_rules.md` in addition when the request is about:

- AR / XR / smart glasses
- premium consumer electronics
- wearables
- futuristic hardware
- product launch pages where the object itself should dominate the experience

In those cases, prefer a hardware campaign structure over a SaaS landing structure.

### Phase 3: Generate Real Copy

Do not use placeholders.

Generate:

1. Navbar labels
2. Headline
3. Supporting text
4. Primary CTA
5. Secondary CTA or bottom widget CTA
6. Badge / micro-label if helpful

Use `resources/copywriting_formulas.md` only as inspiration, not as something to expose verbatim in the final prompt.

### Phase 4: Build the Prompt

Before writing the final prompt, load `resources/prompt_templates.md` and choose the closest scaffold:

- `Template A` for `hero-brief`
- `Template B` for standard `page-rebuild`
- `Template C` for implementation-dense `page-rebuild`
- `Template D` for hardware-first campaign pages

When the page should feel especially high-end, editorial, futuristic, or composition-led, enrich the scaffold with:

- `VISUAL THESIS`
- `COMPOSITION RULES`
- `MATERIAL HIERARCHY`
- `SECTION RHYTHM`

When the page is hardware-first, strongly prefer:

- `Object Reveal`
- `Precision Strip`
- `Immersive Proof`
- `Capability Modes`
- `Materials / Engineering Detail`
- `Reserve / CTA`

Do not default to `features grid -> testimonials -> pricing` unless the user or reference clearly calls for it.

### Phase 5: Expand Only If Needed

Only add these sections when the user asks for deeper implementation.

## Writing Rules

Use these writing rules in every final prompt:

1. Sound decisive.
2. Name exact colors and type choices.
3. Specify where content sits vertically and horizontally.
4. Specify whether the section should feel compact, airy, cinematic, dense, or minimal.
5. Call out one or two signature elements that make the design memorable.
6. Keep the prompt visually led, not framework led.
7. When reconstructing a page from a strong reference, keep the original section rhythm and recurring UI patterns intact.
8. Preserve repeated primitives when they are part of the design language, such as all badges sharing one treatment or all video sections sharing one fade pattern.
9. Describe composition, not just layout modules.
10. Give the hero one dominant visual force.
11. Name the primary, secondary, and tertiary materials when effects matter.
12. Use deliberate pacing instead of giving every section equal visual weight.
13. For hardware pages, treat the product as an object reveal, not a card asset.
14. Prefer compressed technical strips and immersive media over repetitive feature cards when the brand is premium and product-led.

## Anti-Patterns

Avoid these unless the user explicitly wants them:

- Starting with package installation and imports
- Dumping full JSX trees
- Generic phrases like "modern and sleek" without visual specifics
- Default purple gradients
- Overly centered layouts when the reference is top-weighted or left-weighted
- Over-padding that makes the hero feel inflated and template-like
- Treating premium pages like neutral component assemblies
- Giving glow, glass, gradients, particles, and blur equal visual weight
- Describing cards and sections without a clear composition thesis
- Compressing a multi-section reconstruction into an underspecified short brief
- Defaulting premium hardware pages to standard SaaS feature-card structures
- Boxing the hero product inside a neat image container when the page should feel campaign-like

## Special Cases

If the user asks to save the prompt, save it as:

- `[brand]_hero_prompt.md` for hero-only outputs
- `[brand]_landing_prompt.md` for full-page rebuild outputs
