# bitago.com — hero section

The hero from your PDF, rebuilt as a real web page and matched to the mockup.

- `index.html` — the whole section. Open it in any browser.
- `assets/` — the photograph, taken out of your PDF.
- `desktop.jpg`, `tablet.jpg`, `mobile.jpg`, `mobile-lower.jpg` — 1280 / 834 / 390 px.

## How it matches the PDF

The design in your PDF is 1610 × 792. Every position and type size in the stylesheet is
the number measured off that file — `left: calc(170 * var(--u))` is design pixel 170. `--u`
is one design pixel expressed as a fraction of the section's width, so the whole hero scales
as one piece and stays identical to the mockup at any desktop width.

Checked against the PDF, element by element: logo, Log in, Sign up pill, headline (both lines),
sub-heading, both buttons, the promo box (including where its lines break), the three stats
and the Trustpilot line — all within a couple of pixels, all the same size relative to the page.

## The photograph

The PDF is a stack of flat images with the text baked into them, so the copy could not simply
be lifted off. I pulled out the hero image and painted out the text that was burned into it —
the headline, buttons, promo box, stats, the nav, the Trustpilot line and the chat bubble in
the corner. What is left is the clean photograph. All the wording you see is now real HTML
text sitting on top of it, which means it is selectable, searchable, translatable, sharp on
any screen, and editable in WordPress without touching the picture.

**Worth knowing:** the images inside the PDF are 114–141 dpi. That is fine at normal screen
size but will look slightly soft on a high-resolution laptop or a 4K monitor. If you have the
original photograph at full size, send it and it drops straight in.

## Still placeholders

| Item | Status |
|---|---|
| Logo mark | Traced by hand from the PDF. Send the real SVG/PNG and it drops in. |
| Accent teal `#33CBC7` | Sampled off the Sign up button in your PDF. Confirm the exact hex. |
| Typeface | Poppins, the closest free match. Tell me the real font and I'll swap it. |
| Button links | All `#` for now. |

## Responsive behaviour

| Width | What happens |
|---|---|
| ≥ 900px | Exactly the mockup, scaled to the window |
| < 900px | The mockup has no small-screen design, so the same content restacks: copy, buttons, promo, then the photo, then the stats |
| < 420px | Tighter headline, QR button drops out of the header |

Verified at each width: no horizontal scroll and no element pushed outside the viewport.

## In the WordPress build

This becomes the hero section template, with the headline, sub-heading, both button labels and
links, the promo box and all three stat items exposed as editable fields.

Motion is CSS-only (hover lifts on the buttons). No JavaScript, no animation library.
