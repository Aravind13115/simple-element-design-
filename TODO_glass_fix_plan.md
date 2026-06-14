# Glassmorphism fix plan (current file got malformed)

## Information gathered
- The page is a single HTML file: `task1-simple-elements.html`.
- I added glass design tokens + `.glass` helpers, but the CSS now contains a duplicated/unfinished block right after `.glass-plain { ... }`.
- This likely caused the reported CSS parse errors (e.g., `at-rule or selector expected`) and prevents proper styling.

## Plan
1. Repair `task1-simple-elements.html` by removing the malformed duplicated tail of the old `:root` section that starts right after `.glass-plain`.
2. Apply glass styling systematically:
   - Replace solid backgrounds on all containers/cards/modals/tooltip-like surfaces with `background: rgba(255,255,255,0.12)` + `backdrop-filter: blur(20px)`.
   - Ensure borders are `1px solid rgba(255,255,255,0.20)`.
   - Convert white-only mock panels to glass too.
3. Text contrast:
   - Update text colors on glass surfaces to darker tones where background is light-glass.
   - Keep tooltip bubble as dark translucent glass with light text.
4. Add `-webkit-user-select: none` wherever `user-select: none` is present.

## Dependent files
- `task1-simple-elements.html`

## Followup steps
- Open file in browser and visually verify glass edges and readability.
- If any CSS parse errors remain, re-run a quick scan by searching for unmatched braces.

