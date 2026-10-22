# Premium Image — Higgsfield / ChatGPT Prompt

The shipped `social-preview.svg`/`social-preview.png`/`hero.png` are deterministic
vector assets (Higgsfield CLI was installed but not authenticated;
`higgsfield auth login` is a one-time browser OAuth).

## Higgsfield

```bash
higgsfield auth login          # one-time browser login
higgsfield generate create <image-model> --prompt "<prompt below>"
```

## Prompt (paste into ChatGPT gpt-image / Nano Banana Pro / Higgsfield)

```
A premium, minimal tech-keynote hero image for "Awesome Server Stack".
Dark navy background (#0B1020) with a subtle radial glow. On the right, a
3D server rack built from four glowing glass blades edged in a gradient
fading from emerald green (#34D399) to electric blue (#2563EB), status
LEDs lit, thin luminous HTTP request lines streaming from the left edge
into the rack. On the left, bold clean sans-serif typography: small green
caps label "THE 2026 INDEX · 55+ TOOLS", then "Awesome Server Stack" in
large white heavyweight text, tagline below in softer white: "Drop legacy
infra. Benchmarks, not vibes." At the bottom, small muted text: "Caddy ·
Pingora · Elysia · Dragonfly · Coolify · FrankenPHP". Flat vector style
with soft glows, glassmorphism panel behind the text, no photorealism,
no humans, no clutter, wide 2:1 composition, 1280x640.
```

## After generation

- Save as `docs/assets/social-preview.png` (1280×640) — GitHub social preview + README hero.
- Re-render `hero.png` at 1600×800 (`magick social-preview.png -resize 1600x800^ -gravity center -extent 1600x800 hero.png`).
- Keep `social-preview.svg` as the deterministic fallback.
