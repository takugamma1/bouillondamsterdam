# Bouillon d’Amsterdam — merch shop (Shopify Horizon)

Shopify **Horizon 4.3.0** theme configured to look like [bouillondamsterdam.nl](https://www.bouillondamsterdam.nl):
no custom code, only theme settings, section groups and JSON templates.

## Design mapping

| Their site | Theme setting |
| --- | --- |
| Bordeaux `#5C0018` (their "black") | `color_palette.foreground`, bordeaux bands, footer bar, add-to-cart |
| Ink navy `#15102C` announcement bar | `color_palette.color1`, header announcement |
| White crumpled paper background | `assets/bda-paper-background.jpg` as section background image (home hero, collection heading) |
| Bordeaux tint over the interior photo | Hero section, overlay style **gradient**, `#5c0018e6` |
| Transducer / Poppins sans | Poppins 400 / 600 / 700 (body, subheading, heading) |
| Espiritu brush script | Yellowtail (accent font, used by `h1` and `h3` presets) |
| Square 1px outlined buttons | Primary button: transparent, 1px bordeaux border, radius 0 |
| 10px form fields, 12px panels | `inputs_border_radius: 10`, `popover_border_radius: 12` |

## One-time setup in Shopify admin

1. **Connect this repo** — Online Store › Themes › Add theme › Connect from GitHub › `takugamma1/bouillondamsterdam`, branch `main`.
2. **Upload the brand images** to Content › Files with exactly these names (the templates reference them as `shopify://shop_images/...`). Copies are in `assets/`:
   - `bda-icon-bordeaux.png` (header logo + favicon)
   - `bda-logo.png` (footer wordmark)
   - `bda-paper-background.jpg` (paper texture)
   - `bda-westereiffel.png` (Eiffel line drawing in the hero)
   - `bda-food.jpg`, `bda-interior.jpg` (home page photos)
3. **Navigation** — create the `Main menu` (Online Store › Navigation), e.g. *Merch* → `/collections/all`, *Over ons* → `https://www.bouillondamsterdam.nl/overons`, *Contact* → `/pages/contact`.
4. **Products** — add the merch products; the home page and `/collections/all` show them automatically.
5. **Language** — the theme ships Dutch translations (`locales/nl.json`); set Dutch as the store language under Settings › Languages so cart, checkout and system text match the Dutch page copy.
