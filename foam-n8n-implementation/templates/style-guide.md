# REdI FOAM Writing Style Guide

Common patterns across high-quality FOAM content for advanced clinical audiences, published by the **Resuscitation EDucation Initiative (REdI)**, Metro North Health, Queensland.

## Voice and Tone

**Expert-to-colleague register:**
- Write as if explaining to a competent colleague who missed the latest paper
- Assume baseline knowledge; don't over-explain fundamentals
- First person acceptable for reasoning: "I would consider...", "My approach..."
- Avoid didactic/textbook tone

**Intellectual honesty:**
- Acknowledge uncertainty explicitly
- Distinguish evidence quality levels
- Don't fill evidence gaps with confident prose
- State when something is opinion vs evidence

## Formatting Standards

### Structure

| Element | Standard |
|---------|----------|
| Paragraphs | Max 5 sentences |
| Sentences | Average <25 words |
| Sections | 300-500 words before subheading |
| Total length | Case-based: 1,500-2,500 words; Journal club: 1,000-2,000 words; Clinical review: 3,000-5,000 words |

### Visual Hierarchy

**Bold** for:
- Critical thresholds ("QRS >100ms")
- Drug doses
- Key warnings
- Important definitions

*Italics* for:
- Case vignette text
- Emphasis (sparingly)

> Blockquotes for:
> - Key takeaways / clinical pearls
> - Expert quotes with attribution
> - Important summaries

**Headers:**
- Descriptive and actionable ("When to Intubate" not "Airway Management")
- Question format for decision points ("Should we give steroids?")
- Use H2 for main sections, H3 for subsections

### Lists

Use bullets when:
- â‰¥3 related items
- Items are parallel in structure
- Order doesn't matter

Use numbered lists when:
- Sequence matters
- Items will be referenced by number

Each bullet: minimum 5 words, complete thought.

## Evidence Presentation

### Citation Style

Inline with hyperlinks preferred:
```
...demonstrated in the ARISE trial (PMID: 25099709)...
```

Or numbered references:
```
...demonstrated in recent trials (1,2)...
```

Include PMIDs or DOIs for verifiability.

### Trial Naming

Use acronyms readers know:
- ARISE, ProCESS, ProMISe (sepsis)
- CRASH-2, CRASH-3 (TXA)
- EAST, HEAT (paracetamol in sepsis)
- TTM, TTM2 (temperature management)

Expand on first use only if acronym is obscure.

### Numbers and Statistics

Include when available:
- Absolute risk reduction (ARR)
- Number needed to treat (NNT)
- 95% confidence intervals
- p-values (with caution about interpretation)

Example: "...reduced mortality (ARR 2.8%, NNT 36, 95% CI 20-139)"

## Placeholders for Human Input

Mark clearly where clinical expertise is required:

```markdown
[CLINICAL PEARL NEEDED: What bedside signs predict deterioration?]

[EXPERT INPUT NEEDED: Local practice variation for this scenario]

[REGIONAL VARIATION: How does Australian/UK/Canadian practice differ?]

[VERIFY: Dose check required - 4g cited in source but seems high]
```

## Cross-referencing

Link to existing FOAM resources rather than duplicating:
- "For detailed ECG interpretation, see LITFL's [Sgarbossa criteria post](URL)"
- "Previously covered in EM Cases Episode X"

## REdI Visual Identity

All published content must follow the REdI Brand Guidelines. Reference `config/redi-theme.json` for digital design tokens.

### Colour Application

| Element | Colour | Hex | Usage Notes |
|---------|--------|-----|-------------|
| Page headers, section headings | REdI Navy | `#1B3A5F` | ✓ AA compliant on white (11.56:1) |
| Clinical pearl blockquotes (accent border) | REdI Teal | `#2B9E9E` | Accent/border only; use Navy for text (3.24:1) |
| Hyperlinks | Accessible Link Blue | `#0066CC` | ✓ AA compliant on white (5.57:1); alternative: Navy |
| Warning/caution callouts (background) | Warm Yellow | `#F4D03F` | Background only; use Navy/Dark Gray text (1.51:1) |
| Critical alert boxes (text/icon) | Alert Red | `#DC3545` | ✓ AA compliant on white (4.53:1) |
| Success messages (large text only) | Success Green | `#28A745` | Large/bold text only on white (3.13:1) |
| Primary action buttons/CTAs | REdI Coral | `#E55B64` | White text: large/bold only (≥18px or ≥14px bold) |
| Body text | Dark Gray | `#333333` | ✓ AA compliant on white (12.63:1) |
| Page backgrounds | Light Gray / White | `#F5F5F5` / `#FFFFFF` | Use with dark text only |

**Accessibility-compliant colour variants:**
- **Hyperlinks:** Use `#0066CC` (Accessible Link Blue) instead of Sky Blue `#5DADE2` to meet 4.5:1 contrast requirement on white backgrounds
- **Accents vs. Text:** REdI Teal, Sky Blue, and brand Coral should be used as accent colors, borders, or large/bold text only—not for normal body text
- **Button text:** White text on Coral buttons requires minimum 18px font size or 14px bold to meet WCAG 2.1 AA Large criteria

### Typography

- **Primary font:** Montserrat (Regular 400, Medium 500, SemiBold 600, Bold 700)
- **Display font:** Bebas Neue (event titles, promotional headlines only)
- **Body text:** 1rem (16px) minimum, line-height 1.6
- **H1:** 2.5rem, Bold 700
- **H2:** 2rem, SemiBold 600
- **H3:** 1.5rem, SemiBold 600

### Content Branding

Each published piece must include:
- REdI attribution line beneath the title: *REdI — Resuscitation EDucation Initiative | Metro North Health*
- REdI footer: *Published by the Resuscitation EDucation Initiative (REdI), Metro North Health, Queensland.*
- "Powered by REdI" tagline where appropriate

### Accessibility Requirements

All published content must meet **WCAG 2.1 Level AA** compliance:

- **Normal text:** 4.5:1 minimum contrast ratio (applies to body text, small headings, labels)
- **Large text:** 3:1 minimum contrast ratio (≥18px regular or ≥14px bold)
- **Focus indicators:** 3px solid REdI Teal (`#2B9E9E`) outline on all interactive elements
- **Color usage constraints:**
  - Never use Sky Blue `#5DADE2`, Coral `#E55B64`, Teal `#2B9E9E`, or Success Green `#28A745` for normal-sized body text on white/light backgrounds
  - Warm Yellow `#F4D03F` must only be used as a background color with dark text (Navy or Dark Gray)
  - When using white text on Coral backgrounds (e.g., buttons), ensure text is ≥18px or ≥14px bold
- **Keyboard navigation:** All interactive elements must be keyboard-accessible with visible focus states
- Respect `prefers-reduced-motion` for any animated elements
- Maximum line length: 75 characters

## Quality Markers

Content must have:
☐ Named author attribution
☐ Named peer reviewer attribution
☐ REdI branding (header attribution and footer)
☐ Date and update schedule
☐ All claims cited
☐ Explicit uncertainty statements
☐ "Bottom line" summary

## Common Pitfalls to Avoid

- **Hedging without adding information**: "It could be argued that..." (just make the argument)
- **False balance**: Don't present fringe views equally with consensus
- **Premature recommendations**: If evidence is weak, say "evidence is insufficient" not "consider X"
- **Assumed universalism**: Acknowledge practice varies by region/institution
- **Outdated claims**: Flag content needing update if evidence landscape has changed
