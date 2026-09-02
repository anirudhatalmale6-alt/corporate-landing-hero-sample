# bitago.com — hero section

The hero section from your PDF, built as a real web page. One self-contained file, no build
step, no dependencies, no JavaScript.

- `index.html` — the whole section. Open it in any browser.
- `desktop.jpg`, `desktop-stats.jpg`, `tablet.jpg`, `mobile.jpg` — how it renders at 1280 / 834 / 390 px.

## What's rebuilt vs. what's still a placeholder

Rebuilt to match your PDF: the layout, the headline and sub-heading, the Sign up + QR buttons,
the Bitago Premium promo box, the app screen on the phone, and the stats strip with the
Trustpilot rating.

Placeholders, because I don't have the source files yet:

| Item | Status |
|---|---|
| Logo mark | Traced by hand from the PDF. Send the real SVG/PNG and it drops straight in. |
| Accent teal `#33CBC7` | Sampled off the Sign up button in your PDF. Confirm the exact hex. |
| Typeface | Plus Jakarta Sans, the closest free match to your PDF. Tell me the real font. |
| Hero background | Your PDF uses a photo of a hand holding a phone. I don't have that file, so this is a CSS gradient. |

Nothing here uses a Nexo, defi.com or Bybit asset. The phone, the app screen, the icons and
the Trustpilot star are all drawn in CSS and inline SVG.

## Swapping in your brand

Everything visual comes off the variables at the top of the stylesheet:

```css
:root{
  --bg:#050708;      /* page background     */
  --ink:#FFFFFF;     /* headings            */
  --muted:#AFB5BE;   /* body copy           */
  --accent:#33CBC7;  /* buttons, highlights */
}
```

Change `--accent` and the buttons, links and glow all follow. Text and the logo are plain HTML.

## Responsive behaviour

| Width | What changes |
|---|---|
| ≥ 980px | Two columns, copy left, phone right, stats in a row with Trustpilot right-aligned |
| 560–980px | Single column, Log in hidden, menu button appears, stats wrap |
| < 560px | Tighter type, QR button hidden from the header, stats stack |

Verified at each width: no horizontal scroll, nothing clipped, no element pushed outside the
viewport, and nothing overflowing the phone screen.

## In the WordPress build

This becomes the hero section template, with the headline, sub-heading, both button labels and
links, the promo box and all four stat items exposed as editable fields — so you change wording
yourself without touching code.

Motion is CSS-only (a slow float on the phone, hover lifts on the buttons). No JavaScript and no
animation library, which is most of why it loads fast.
