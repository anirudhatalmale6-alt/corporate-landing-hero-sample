# Hero section — free sample

A hand-built sample of the hero section from your Canva mockup (page 1), made so you can judge
build quality before committing to anything.

## What's here

- `index.html` — the whole section, self-contained. One file, no build step, no dependencies.
- `desktop.png`, `tablet.png`, `mobile.png` — how it renders at 1280 / 834 / 390 px wide.

Open `index.html` in any browser. That's it.

## What it is (and isn't)

This is the **layout, styling and motion** rebuilt from scratch — not a copy of anyone's assets.

- No Nexo, defi.com or Bybit images, logos, copy or fonts are used anywhere.
- The phone, the app screen, the chart, the card icons and the rating stars are all drawn in
  CSS and inline SVG. Nothing is a stock photo or a screenshot.
- "Vaultline", the mark, the teal, the numbers and the wording are **placeholders**. They exist
  so the section isn't full of grey boxes. All of it swaps out for yours.

## Swapping in your brand

Everything visual is driven from the variables at the top of the stylesheet:

```css
:root{
  --bg:#07080B;      /* page background       */
  --ink:#FFFFFF;     /* headings              */
  --muted:#9BA1AD;   /* body copy             */
  --accent:#2ED3B7;  /* buttons, highlights   */
  --accent-ink:#04231F; /* text on the accent */
}
```

Change `--accent` and the buttons, the chart, the highlight word, the stars and the glow all
follow. Text and the logo are plain HTML — edit them in place.

## Responsive behaviour

| Width      | What changes                                                        |
|------------|---------------------------------------------------------------------|
| ≥ 980px    | Two columns, copy left, phone right, floating badges, 4-across stats |
| 560–980px  | Single column, nav collapses to a menu button, stats go 2×2          |
| < 560px    | Tighter type and spacing, floating badges hidden, stats stack        |

Checked at each width: no horizontal scroll, nothing clipped off-screen.

## On the WordPress build

The final page is WordPress. This markup becomes the hero section template there, with the
headline, sub-heading, both button labels and links, the promo strip and all four stat items
exposed as editable fields — so you can change the wording yourself without touching code.

Motion is CSS-only (a slow float on the phone and badges, hover lifts on the buttons). No
JavaScript and no animation library, which is most of why it loads fast.
