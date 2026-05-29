# Devlog - 2026-05-29

## Summary

Built a multi-stage front-end learning demo with isolated stage files, root navigation, deployment planning, GitHub Pages workflow, and iterative homepage button alignment fixes.

## Work Completed

### 1. Project structure and stage scaffolding

- Implemented root landing page and visual theme.
- Added three independent stage directories, each with its own HTML and CSS.
- Ensured each stage includes a Back to index navigation path.

Created stage paths:

- `stage-1-semantic-bem/index.html`
- `stage-1-semantic-bem/styles.css`
- `stage-2-tailwind/index.html`
- `stage-2-tailwind/styles.css`
- `stage-3-design-components/index.html`
- `stage-3-design-components/styles.css`

### 2. Stage content implementation

- Stage 1: Semantic HTML and BEM conventions.
- Stage 2: Tailwind CSS demo using Tailwind browser CDN plus a small stage-local CSS enhancement.
- Stage 3: Design components and composition (cards, buttons, badges, panel composition), replacing the earlier web components API direction.

### 3. Home page integration

- Implemented root index navigation cards for all three stages.
- Added card-specific accent button colors.
- Applied introductory hero section and responsive grid layout.

### 4. Planning and documentation

- Wrote repository plan file to make implementation approach visible to students.
- Updated repository README with:
  - Stage structure overview.
  - GitHub Pages hosting instructions.
  - Expected Pages URL format guidance.

### 5. GitHub Pages deployment setup

- Added workflow:
  - `.github/workflows/pages.yml`
- Workflow features:
  - Trigger on push to `main`.
  - Manual trigger via `workflow_dispatch`.
  - Static artifact upload and deploy to GitHub Pages.

### 6. Button sizing/alignment debugging on home page

Addressed mismatch where Stage 2 button appeared taller and later clarified root cause as card-content-length pressure.

Fix iterations:

1. Normalized link rendering with `inline-flex`, centering, explicit line-height, and minimum/fixed vertical sizing.
2. Refined button box model to remove glyph-descender influence from perceived height.
3. Added card grid row structure to align all action links to the end of each card area:
   - `grid-template-rows: auto 1fr auto;`
   - `align-self: end;` on stage buttons.

Result:

- Stage buttons now align to the bottom row of each card consistently, independent of content length.

## Files Added Today

- `PLAN.md`
- `DEVLOG.md`
- `.github/workflows/pages.yml`
- `stage-1-semantic-bem/index.html`
- `stage-1-semantic-bem/styles.css`
- `stage-2-tailwind/index.html`
- `stage-2-tailwind/styles.css`
- `stage-3-design-components/index.html`
- `stage-3-design-components/styles.css`

## Files Updated Today

- `index.html`
- `style.css`
- `README.md`

## Validation Performed

- Checked diagnostics for all created/updated files during implementation.
- No file-level errors were reported in the validation pass.

## Notes for Next Session

- Optional: adjust GitHub Pages workflow trigger if deployment should also run from `tailwind_css` during active development.
- Optional: add screenshots/GIF previews for each stage in README for student onboarding.
