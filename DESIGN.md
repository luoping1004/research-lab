# Design

## Source of truth

- Status: Active
- Last refreshed: 2026-08-06
- Primary product surfaces: Lab overview, team, projects, research, teaching, blog, and contact pages.
- Evidence reviewed: `_config.yaml`, `_includes/header.html`, `_includes/feature.html`, `index.md`, `team/index.md`, `projects/index.md`, `research/index.md`, `teaching/index.md`, `blog/index.md`, `contact/index.md`, and `_styles/`.

## Brand

- Personality: Scholarly, approachable, credible, and concise.
- Trust signals: Named researchers, institutional affiliation, publications, research projects, and direct contact details.
- Avoid: Promotional claims, decorative clutter, and visual patterns that compete with the research content.

## Product goals

- Goals: Explain the lab's work, people, teaching, and opportunities; make key content easy to find.
- Non-goals: Function as a learning-management system or host interactive course delivery.
- Success signals: Visitors can quickly locate research, courses, team members, and contact information.

## Personas and jobs

- Primary personas: Prospective students, collaborators, researchers, course participants, and members of the public.
- User jobs: Understand the lab's focus, review its work, find courses taught by the principal investigator, and make contact.
- Key contexts of use: Desktop and mobile browsing, often reached through search or institutional referrals.

## Information architecture

- Primary navigation: Team, Projects, Research, Teaching, Blog, Contact.
- Core routes/screens: `/`, `/team/`, `/projects/`, `/research/`, `/teaching/`, `/blog/`, `/contact/`.
- Content hierarchy: Page title first, followed by a brief contextual label or introduction, then scannable content. The homepage places Latest News before Highlights so timely updates are visible without changing the primary navigation.

## Design principles

- Reuse the site's existing layouts, includes, icons, and content patterns.
- Keep academic information direct and easy to scan.
- Tradeoffs: Prefer consistency and clarity over adding page-specific visual treatments.

## Visual language

- Color: Use the existing Sass theme and dark-mode palette.
- Typography: Use the existing heading, body, and Google Font configuration.
- Spacing/layout rhythm: Follow existing Markdown page and `section.html` spacing.
- Shape/radius/elevation: Reuse existing component styles; do not add page-specific treatments.
- Motion: Use only existing site interactions and transitions.
- Imagery/iconography: Use existing Font Awesome icons and cohesive, text-free course illustrations in the site's navy, cyan, violet, and magenta visual language.

## Components

- Existing components to reuse: Default layout, header navigation, page headings, icons, sections, lists, buttons, cards, figures, post excerpts, and the compact homepage news list.
- New/changed components: None; Teaching reuses the existing alternating feature component for course image, title, and introduction blocks.
- Variants and states: Follow the site's existing light, dark, desktop, and mobile states.
- Token/component ownership: `_styles/`, `_includes/`, and `_layouts/` remain authoritative.

## Accessibility

- Target standard: Preserve accessible semantic HTML and aim for WCAG 2.1 AA readability.
- Keyboard/focus behavior: Retain the existing keyboard-operable header navigation and links.
- Contrast/readability: Use existing theme colors and readable text hierarchy.
- Screen-reader semantics: Use ordered headings and native lists for course content.
- Reduced motion and sensory considerations: Do not introduce new motion or sensory-only cues.

## Responsive behavior

- Supported breakpoints/devices: Existing responsive behavior across mobile and desktop.
- Layout adaptations: Let the shared header and content layout handle narrow screens.
- Touch/hover differences: Keep content available without relying on hover.

## Interaction states

- Loading: Static content requires no dedicated loading state.
- Empty: Omit empty content sections.
- Error: Use the existing `404.md` behavior.
- Success: Not applicable to static informational pages.
- Disabled: Not applicable.
- Offline/slow network, if applicable: Core text remains usable without remote media.

## Content voice

- Tone: Clear, professional, welcoming, and factual.
- Terminology: Use standard academic labels such as Research, Teaching, Courses, and Blog.
- Microcopy rules: Prefer short labels and sentence case; identify personal teaching activity explicitly when needed.

## Implementation constraints

- Framework/styling system: Jekyll, Liquid, Markdown, and the repository's Sass partials.
- Design-token constraints: Reuse existing variables and theme rules; add no parallel token system.
- Performance constraints: Prefer static content and existing assets; add no dependencies for simple pages.
- Compatibility constraints: Preserve the current Jekyll and GitHub Pages build flow.
- Test/screenshot expectations: A production Jekyll build must succeed after navigation or page changes.

## Open questions

- None for the current Teaching page.
