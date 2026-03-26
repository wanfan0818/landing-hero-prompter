# landing-hero-prompter

High-fidelity landing page prompt generator.

This skill is for people who want an AI coding assistant to produce a landing hero section, or reconstruct a full landing page, in a way that actually feels designed, not just assembled from common SaaS tropes.

## Install

```bash
npx skills add wanfan0818/landing-hero-prompter
```

## Modes

### `hero-brief`

Use this when the user wants a concise but art-directed hero prompt.

### `page-rebuild`

Use this when the user provides a section-by-section reference and wants the page reconstructed with recurring patterns, custom effects, and richer implementation detail.

## Routing Logic

Use the closest matching pattern instead of treating every request as generic SaaS:

- dark analytics hero -> `examples/dark_saas.md`
- light fintech hero -> `examples/light_fintech.md`
- creative glass full page -> `examples/glass_creative.md`
- logistics / industrial page -> `examples/cinematic_dark_logistics.md`
- Apple-like glass rebuild -> `examples/apple_glass_full_page.md`
- sustainability / impact editorial page -> `examples/editorial_impact_full_page.md`
- green-accent revenue SaaS page -> `examples/green_glass_saas_full_page.md`

If a strong reference is provided, follow the reference over the default category mapping.

## Resources

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

## Examples

- `examples/dark_saas.md`
- `examples/glass_creative.md`
- `examples/light_fintech.md`
- `examples/cinematic_dark_logistics.md`
- `examples/apple_glass_full_page.md`
- `examples/hardware_campaign.md`
- `examples/editorial_impact_full_page.md`
- `examples/green_glass_saas_full_page.md`

## Notes

- Use exact values whenever they matter visually.
- Generate real copy instead of placeholders.
- Respect the reference image composition if one is provided.
- For premium, futuristic, or editorial pages, define a visual thesis, composition rules, material hierarchy, and section rhythm before listing sections.
- For AR, XR, or premium hardware pages, prefer an object-reveal structure over a generic SaaS section stack.
- Preserve named custom components and repeated section patterns when reconstructing full pages.
- Reuse the scaffold in `resources/prompt_templates.md` instead of inventing a new output shape each time.

## License

MIT
