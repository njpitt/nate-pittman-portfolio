# Nate Pittman Portfolio — Project Context for Claude

## About the User
Nate is a Senior Product Designer at Ulta Beauty with no coding background. Explain things in plain language, break changes into small steps, and always pause for confirmation before making large edits.

## Tech Stack
- Plain HTML and CSS — no JavaScript framework, no build tools
- No npm or node required
- Files open directly in the browser (no local server needed)

## File Structure
```
index.html          ← Home page (only page for now)
css/
  tokens.css        ← Design tokens: all colors, fonts, sizes as CSS variables
  style.css         ← Global styles + all section styles
assets/
  images/           ← Case study images, headshot, thumbnails
```

## Design System
- **Figma file key:** 7dL14kETqa19GqzoLoWko9 (Personal Portfolio Site)
- **Figma frame size:** Mobile-first, 390px frames
- **Background:** `--color-background: #FAF8F5` (warm off-white)
- **Accent:** `--color-accent: #1558D6` (Electric Cobalt)
- **Heading font:** Playfair Display (`--font-display`)
- **Body font:** DM Sans (`--font-body`)
- **No dark mode**

Always reference CSS tokens from `tokens.css` — never use hardcoded hex values in `style.css`.

## Deployment
- GitHub repo: njpitt/nate-pittman-portfolio
- Vercel auto-deploys on every push to `main`
- Live site updates ~30 seconds after a push

## Branch Strategy
- `main` = always the working, deployed version
- New sections get their own branch: `feature/home-hero`, `feature/home-case-studies`, etc.
- Merge to main only after Nate has reviewed in browser

## Workflow (Figma → Code)
1. Nate shares a Figma frame URL
2. Claude reads it with `get_design_context`
3. Claude translates one section at a time — never the full page at once
4. Nate reviews in browser before committing
5. Claude commits and pushes; Vercel deploys

## CSS Organization
Sections in `style.css` are separated by named comment blocks:
```css
/* =====================
   SECTION NAME
   ===================== */
```

## Featured Case Studies
1. Recently Viewed Rail in Search — 18% vs 8% conversion lift, shipped
2. Filters & Guided Navigation — strategic vision, $50M–$150M ARR analysis, not shipped
3. Ulta AI Integration — strategy lead, MVP live, built with Google ⚠️ needs manager approval before publishing
