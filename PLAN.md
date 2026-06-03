## Implementation Plan: Multi-Stage HTML/CSS Demo + GitHub Pages

Build a three-stage demo site linked from a single homepage, where each stage has its own HTML and CSS file: semantic HTML + BEM, Tailwind CSS, and design components + composition (without Web Components API). Use folder-based stage routes to keep assets isolated and prevent CSS conflicts, then publish via GitHub Pages so students can view it live.

### Steps

1. Phase 1 - Structure setup.
2. Create stage directories and isolated asset pairs.
3. Add Stage 1 files for semantic HTML + BEM using meaningful sectioning elements and BEM class naming.
4. Add Stage 2 files for Tailwind CSS demo with Tailwind CDN and optional local stage polish CSS.
5. Add Stage 3 files for design components and composition using reusable CSS classes.
6. Phase 2 - Navigation and consistency.
7. Build root index page with links to all three stage pages and short learning goals.
8. Ensure each stage includes a visible Back to index link and accessibility basics.
9. Phase 3 - GitHub Pages hosting.
10. Add student-facing GitHub Pages documentation.
11. Add a GitHub Actions workflow for static Pages deployment.
12. Ensure relative links and asset paths so the project works both locally and on Pages.
13. Phase 4 - Validation.
14. Validate local routing and stage-specific CSS imports.
15. Validate hosted behavior after Pages deploy.
16. Verify styling boundaries and semantic quality.

### Relevant Files

- index.html
- style.css
- stage-1-semantic-bem/index.html
- stage-1-semantic-bem/styles.css
- stage-2-tailwind/index.html
- stage-2-tailwind/styles.css
- stage-3-design-components/index.html
- stage-3-design-components/styles.css
- .github/workflows/pages.yml
- README.md

### Verification Checklist

1. Run local server: pip3 install flask && python3 server.py.
2. Open /, /stage-1-semantic-bem/, /stage-2-tailwind/, /stage-3-design-components/.
3. Confirm each stage only imports its own styles.css.
4. Confirm Stage 1 follows BEM naming patterns.
5. Confirm Stage 2 loads Tailwind CDN and renders utility classes.
6. Confirm Stage 3 reuses component classes in multiple composed sections.
7. Confirm GitHub Pages deployment publishes successfully and links do not 404.
8. Spot-check headings, focus states, and contrast.
