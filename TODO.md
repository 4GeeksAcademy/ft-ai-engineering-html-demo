# TODO: Dark Mode Toggle Troubleshooting

## Context
The dark mode toggle button was not visibly changing theme styles in the Tailwind CDN setup.

## Troubleshooting Steps Taken
1. Verified toggle script execution in [index.html](index.html):
   - Confirmed click handler was toggling the `dark` class on `document.documentElement`.
   - Confirmed preference was being written to `localStorage` (`theme = dark|light`).
2. Checked Tailwind dark variant behavior:
   - Confirmed `dark:*` utility classes were present throughout layout components.
   - Identified likely mismatch between class toggling and Tailwind dark-mode variant configuration.
3. Attempted custom variant setup:
   - Added a `@custom-variant` rule for dark mode in a Tailwind style block.
   - Result: editor diagnostics reported `Unknown at rule @custom-variant`.
4. Applied CDN configuration-based fix:
   - Added global Tailwind config before CDN script:
     - `tailwind = { config: { darkMode: "class" } }`
   - Removed custom at-rule approach to eliminate diagnostics.
5. Improved UX and accessibility:
   - Added dynamic button label updates (`Switch to dark` / `Switch to light`).
   - Added `aria-pressed` updates to reflect current state.

## Current Status
- Diagnostics in [index.html](index.html) show no errors.
- Theme toggle should now apply class-based dark mode correctly.

## Follow-Up (If Issue Reappears)
1. Hard refresh browser to clear stale CDN script cache.
2. Inspect `<html>` element to confirm `dark` class toggles on click.
3. Verify dark utilities are generated and applied in computed styles.
4. Temporarily remove `localStorage` logic to isolate state initialization issues.
5. Confirm no conflicting scripts are overriding `document.documentElement.className`.
6. If needed, migrate from CDN runtime compilation to a local Tailwind build for deterministic output.
