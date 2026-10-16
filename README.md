# BIA (Case Study) — web rebuild

A responsive web rebuild of the **BIA (Case Study)** page from the Rhapsody Figma file
*BIA Re-Introduction* (`gNduebUl4fwpFjWYJwzDgo`, frame `3:5062`), built for Jamie Bitmead,
16 Oct 2026.

**Live:** https://bia-case-study.vercel.app

## What was taken from the original
- Copy: verbatim (headline, lede, "Rhapsody Utilisation:", all 8 capability tags).
- Palette: read off the file, not sampled — `#1C0D52` ground, `#D9B3F3` lede,
  `#D2B4ED` pills / sub-head / the underscore in `BIA_`.
- Layout: collage positions derived from the real frame coordinates and expressed as
  percentages of a `1068 × 848` box, so the arrangement survives any viewport.

## Images
Every image is **my own export**, pulled through `GET /v1/images/:key` as a rendered
group — so each one arrives with its mask already applied, rather than being the raw
Shutterstock source re-used in place. PNG @2x → WebP q86: **3.87 MB → 316 KB (8%)**.

| asset | source node |
|---|---|
| `photo-lab.webp` | `3:5091` |
| `photo-team.webp` | `3:5097` |
| `photo-screen.webp` | `3:5102` |
| `photo-circle.webp` | `3:5107` |
| `photo-strip.webp` | `3:5114` |
| `mark-vertical.svg` | `3:5064` (vertical "Rhapsody" wordmark) |

## Fonts — substituted, and this is a real difference
The original sets **FAM Aime Light 100** for `BIA` and **Rhapsody Favorit** for everything
else. Neither is installed on this host and neither is web-licensed here, so:

- `BIA` → **Cormorant Garamond 300** (closest free high-contrast serif)
- body, sub-head, pills → **Inter** — which the original already uses for the pills

Swap in the real webfonts and it will match exactly; nothing else needs to change.

## Adjusted for web
- Collage holds its designed arrangement down to 620px, then reflows to a 2-column grid.
- Entrance animation on load, disabled under `prefers-reduced-motion`.
- Alt text written per image; `noindex` set, since the imagery is licensed stock.
