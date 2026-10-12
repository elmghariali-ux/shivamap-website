# ShivaMap website redesign

Static homepage redesign for shivamap.es. Plain HTML, CSS and a few lines of vanilla JS, with no build step and no framework.

- Live preview: https://shivamap-website.vercel.app
- Deploys automatically to Vercel on every push to `main`

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole page: markup, inline styles, and a small script at the bottom |
| `assets/logo.png` | ShivaMap logo |
| `assets/map_spain.jpg` | Static screenshot of the current map (hero) |
| `assets/map_night.jpg` | "Night map" image for the dark band section |
| `vercel.json` | `cleanUrls` only |
| `robots.txt` | Allows indexing |

Fonts come from Google Fonts (Archivo for headings, DM Sans for body).

## Brand tokens

| Token | Hex |
| --- | --- |
| Navy (background) | `#060d1f` |
| Brand blue | `#1a6dbf` |
| Light blue | `#4db8ff` |
| Gold | `#ffd166` |
| Green | `#4cdf80` |

## What is a placeholder (needs wiring to the real app)

1. **Hero map**: a static image. Replace with the real interactive map component.
2. **Search box** ("Ciudad, barrio o código postal") and the **"Cerca de mí"** button: no action yet. Should search the map and use geolocation.
3. **Category buttons** (Clubs / GrowShops / Tiendas CBD): only toggle their own style and the "Mostrando:" label. Should filter the map, or link to `/es/mk_clubscannabis`, `/es/mk_growshops`, `/es/mk_cbd`.
4. **Example place card** shows `[Nombre del club]` and `[Barrio, Ciudad]`. Its WhatsApp, Instagram and "Cómo llegar" buttons should use each marker's real data.
5. **Map / Satélite** switch is visual only.
6. **App Store / Google Play badges** link to `#app`. Real links:
   - https://apps.apple.com/app/shivamap/id6470916555
   - https://play.google.com/store/apps/details?id=com.gestionverde.shivamap
7. **Nav and footer links** use in-page anchors. Map them to the real routes: `/es/lista` (Mis marcadores), `/es/shiva` (Área profesional), `/es/shiva/tos` (Términos), `/es/shiva/tos#cookies`, `/SponsorsShivaMapES.pdf`.
8. **Language button** shows "ES" only. Hook it to the existing `/en`, `/de`, `/fr`, `/pt`, `/it`, `/nl` versions.

## Content notes

- Only features that exist on the current site are described: validated places, WhatsApp/Instagram chat, Google Maps route, map/satellite, saved markers, 7 languages, free pro listing.
- The page includes an 18+ and "uso responsable" note that matches the terms. Keep it.
- Responsive down to ~390px. On phones the text nav links and "Área profesional" button are hidden; a mobile menu would be a good addition.
