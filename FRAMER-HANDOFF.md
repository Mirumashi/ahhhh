# PharmaGo — Framer handoff

The current store remains a multi-page HTML demo. Framer cannot turn this project into native editable canvas layers automatically, but the visual system below is deliberately small and can be recreated as editable Framer styles and components.

## Variables

| Framer variable | Value | Use |
| --- | --- | --- |
| `Ink` | `#18322B` | Headings and primary text |
| `Forest` | `#176B57` | Primary action and logo |
| `Cream` | `#F7F4EE` | Page background |
| `Mint` | `#ECF8F2` | Quiet surfaces and active tabs |
| `Lilac` | `#C4B5FD` | Decorative accent only |
| `Coral` | `#FFB59F` | Decorative accent only |

## Components to make editable in Framer

1. **Floating Nav** — max width 1120, 22px radius, white 86% background, 12px top offset.
2. **Hero Care Card** — 32px radius, dark green gradient, abstract circles and a pill icon. Keep the text and icon as separate layers.
3. **Product Card** — 22px radius; product image wrapper uses a fixed **4:3** aspect ratio and `Cover` fit. Do not size cards from the source image.
4. **Status Pill** — 999px radius, 10–12px type, semantic colour variants.

## Image rule

Export or upload product images at **1200 × 900 px** (4:3). In Framer set the image layer to `Fill` / `Cover` and centre it. This gives every product card the same image window regardless of the original upload dimensions.

## Recommended Framer structure

`Page → Floating Nav → Hero (Text + Hero Care Card) → Category Pills → Product Grid → Footer`

The current implementation keeps the same structure in `index.html`; it can be rebuilt component-for-component in Framer without changing the content model.
