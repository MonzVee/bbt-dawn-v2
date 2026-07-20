# BBT — Better Battery Tyres | Claude Code Context File
**Store:** 01jkmb-hf.myshopify.com | **Domain:** betterbattery.co.za
**Theme:** Dawn (bbt-dawn) | **Repo:** github.com/MonzVee/bbt-store
**Last updated:** June 2026

---

## 1. BUSINESS CONTEXT

Better Battery Tyres (BBT) is a South African automotive retail and fitment business.

- **Physical location:** 140 Modderfontein Road, Tembisa (also serves Midrand)
- **Phone / WhatsApp:** 063 500 1740
- **Email:** hello@betterbattery.co.za
- **Google reviews:** 24 × five-star | Review link: g.page/r/CURQ3dL5N-RjEBM/review
- **Social:** facebook.com/betterbattery | instagram.com/betterbattery_shop | tiktok.com/@betterbattery

### Core revenue channels
| Channel | Products | Model |
|---------|----------|-------|
| In-store | Batteries, tyres, combos, fitment | Walk-in + WhatsApp leads |
| Online (Shopify) | Accessories, oils, all products | Nationwide delivery + click & collect |
| WhatsApp | All products via Ntombi AI agent | Broadcast + inbound leads |
| B2B Workshop Trade | Oils, batteries, consumables | Monthly trade accounts |

### Target customers (priority order)
1. Taxi / minibus operators — Toyota Quantum, NV350, HiAce
2. Uber / Bolt 7-seater drivers — Toyota Avanza, Rumion, Suzuki Ertiga
3. Passenger car owners — Polo Vivo, Hilux, Swift, Corolla, i10/i20
4. Independent workshops and mechanics (B2B)

---

## 2. BRAND DESIGN SYSTEM

### Colour palette (apply everywhere — no exceptions)
```css
:root {
  --bbt-gold:   #F5C000;   /* Primary — CTAs, prices, highlights, star ratings */
  --bbt-black:  #111111;   /* Page background, navbar, product cards */
  --bbt-dark:   #1D1D1D;   /* Card backgrounds, input fields, surfaces */
  --bbt-surface:#2A2A2A;   /* Borders, dividers, secondary surfaces */
  --bbt-cream:  #E8E0C8;   /* Body text on dark backgrounds */
  --bbt-muted:  #888888;   /* Secondary labels, captions */
  --bbt-wa:     #25D366;   /* WhatsApp CTAs exclusively */
  --bbt-red:    #E53935;   /* Badges, flash sale, urgency */
  --bbt-border: 1px solid #2A2A2A;
  --bbt-radius: 10px;
  --bbt-radius-sm: 6px;
}
```

### Typography
- Font stack: `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- Heading weight: 700 — product names, section titles, prices
- Price display: weight 800, `var(--bbt-gold)`, minimum 18px
- All caps: section labels, badges, category names only

### Design principles
- **Dark theme throughout** — `#111111` background, gold accents
- **Mobile-first** — all layouts designed for 390px viewport first
- **WhatsApp-first** — WhatsApp CTA on every product, in bottom nav, sticky banner
- **Gamified** — spin wheel, flash sale countdown, loyalty points bar
- Inspired by: Temu layout energy + Tyremart category structure

---

## 3. COLLECTIONS (7 total — automated tag rules)

| Handle | Display name | Auto-tag rule |
|--------|-------------|---------------|
| `taxi-minibus` | Taxi & Minibus | quantum OR np350 OR hiace OR 195-14c OR 195-15c OR taxi-battery OR taxi-tyre OR taxi-combo |
| `7-seater` | 7-Seater | avanza OR rumion OR ertiga OR 7-seater OR 7-seater-battery OR 7-seater-tyre OR 7-seater-combo OR 185-70-14 |
| `passenger-cars` | Passenger Cars | passenger OR polo-vivo OR hilux OR swift OR corolla OR passenger-battery OR passenger-tyre |
| `service-kits` | Service Kits | service-kit |
| `oils-fluids` | Oils & Fluids | engine-oil OR oil OR fluid OR lubricant |
| `car-accessories` | Car Accessories | accessory OR gadget OR interior OR lighting OR security OR dash-cam OR obd2 OR led |
| `workshop-trade` | Workshop Trade | Landing page only — no product grid |

**SEO titles:**
- taxi-minibus: "Quantum Tyres, Batteries & Rim Combos | BBT Tembisa"
- 7-seater: "Avanza Rumion Ertiga Combos & Tyres | BBT Tembisa"
- passenger-cars: "Car Batteries & Tyres Tembisa Midrand | Better Battery Tyres"
- car-accessories: "Car Accessories & Gadgets South Africa | Better Battery Tyres"
- oils-fluids: "Engine Oil In Stock Tembisa | Shell & Liqui-Moly | BBT"
- service-kits: "Car Service Kits South Africa | BBT Fitment Centre"

---

## 4. PRODUCT CATALOGUE

### Global product rules
- All prices in ZAR whole numbers — no decimals (R700 not R700.00)
- Compare-at price = selling price × 1.15, rounded to nearest R10
- WhatsApp CTA in every description: "Need help choosing? WhatsApp us on 063 500 1740 — we reply in minutes."
- `status: active` = CONFIRMED in stock | `status: draft` = VERIFY / price TBC
- Vendor: "Better Battery Tyres" on all products
- Metafield `custom.gp_floor` = 25 (25% GP floor — never go below)

### 4A. Batteries

#### Osaka Car Battery (value tier) — status: active
Tags: battery, osaka, passenger-battery, 7-seater-battery, taxi-battery
Scrap deposit: R250 — discount code TRADE250 applied at counter on collection

| Variant | Price | Fitment |
|---------|-------|---------|
| 616 — 45AH | R700 | Toyota Rumion, Suzuki Ertiga, Kia Picanto, Hyundai i10, Honda Jazz |
| 618 — 50AH | R750 | Toyota Conquest, Hyundai i20, VW Polo Vivo, Ford Fiesta (2007+), Nissan Micra |
| 628 — 60AH | R950 | Toyota Corolla, VW Polo, Nissan NP200, Ford Figo, BMW Mini (2002+) |
| 646 — 70AH | R1,100 | Ford Fiesta/Focus, VW Jetta/Golf 6/Tiguan, Toyota Corolla (2007+), Opel Astra |
| 652 — 74AH | R1,350 | VW Golf (petrol), Ford Focus RS, Toyota Hilux (petrol), VW Passat |

#### Exide Eco Car Battery (premium tier) — status: active
Tags: battery, exide, passenger-battery, 7-seater-battery, taxi-battery, premium-battery
Scrap deposit: R475 — discount code TRADE475 applied at counter on collection

| Variant | Price | Fitment |
|---------|-------|---------|
| 619 — 45AH | R1,150 | VW Polo Vivo, Suzuki Swift, Toyota Starlet, Hyundai Atos |
| 628 — 60AH | R1,300 | Toyota Avanza/Rumion/Ertiga/Corolla, BMW Mini (2002+) |
| 646 — 70AH | R1,450 | Ford Fiesta/Focus, VW Jetta/Golf/Tiguan, Toyota Corolla (2007+) |
| 652 — 74AH | R1,650 | VW Golf/Passat, Toyota Hilux (petrol/2.5D), Ford Ranger T6 petrol |
| 657 — 80AH | R1,650 | Toyota Hilux D4D, BMW 3/5 Series diesel, Audi A6/A8/Q7, Ford Ranger 3.2D, Range Rover Sport |
| 658 — 88AH | R2,200 | BMW 7 Series/X5/M3/M5, Audi A6/A8/Q7/RS4, Mercedes C/E/S/ML Class, Porsche Cayenne/911 |
| 668 — 95AH | R2,150 | BMW 1/3 Series stop-start, BMW X1/Z4, Audi A3/A5/Q3/Q5, Mercedes A/S Class, Range Rover Evoque |

**IMPORTANT — Exide 668:** Confirm SMF or AGM technology with supplier before publishing.
Start-stop vehicles require AGM. Wrong technology = returns.

**Battery shipping profile:** Click & collect FREE | Local delivery 10km radius R80 | No nationwide delivery.

**Scrap deposit mechanic (Option C):**
All battery prices shown WITH trade-in (deposit included in price).
Customer brings old battery at collection → staff apply discount code at counter.
Never adjust this at checkout — handled in-store only.
Product description must include: "Price includes scrap deposit. Bring your old battery and save R250 (Osaka) or R475 (Exide)."

### 4B. Tyres

**Shipping profile:** Click & collect FREE | Per-tyre delivery fee R80 local / R120 nationwide

#### 185/70/14 Tyre — status: active
Tags: tyre, 7-seater, 7-seater-tyre, avanza, rumion, ertiga, 185-70-14
Fitment: Toyota Avanza, Rumion, Suzuki Ertiga, Toyota Corolla — per tyre

| Variant | Price |
|---------|-------|
| BSW Import (Black Sidewall) | R850 |
| WSW Import (White Sidewall) | R1,150 |
| WSW LMC / Linglong | R1,250 |
| WSW Hockenheim Vanza | R1,350 |

#### 195/14C Tyre — status: active
Tags: tyre, taxi-tyre, quantum, np350, hiace, 195-14c
Fitment: Toyota Quantum, NV350, HiAce — per tyre

| Variant | Price |
|---------|-------|
| BSW (Black Sidewall) | R1,100 |
| WSW (White Sidewall) | R1,200 |

#### 195/15C Tyre — status: active
Tags: tyre, taxi-tyre, quantum, 195-15c
Fitment: Toyota Quantum (15-inch rim) — per tyre

| Variant | Price |
|---------|-------|
| BSW (Black Sidewall) | R1,200 |
| WSW (White Sidewall) | R1,300 |

#### Passenger Car Tyre — Import — status: active
Tags: tyre, passenger-tyre, passenger
One parent product, size as variant — per tyre

| Size | Price | Fitment note |
|------|-------|-------------|
| 175/70/13 | R750 | Small hatchbacks |
| 155/80/13 | R750 | Small hatchbacks |
| 175/65/14 | R850 | Starlet, Swift, Palio |
| 185/60/14 | R850 | Various 14-inch |
| 185/60/15 | R950 | Various 15-inch |
| 185/65/15 | R950 | Various 15-inch |
| 195/65/15 | R1,100 | VW Polo Classic, Corolla |
| 195/50/15 | R950 | Performance 15-inch |
| 205/55/16 | R1,150 | Golf, Astra, 16-inch |
| 205/40/17 | R1,100 | Low-profile 17-inch |
| 215/45/17 | R1,250 | Low-profile 17-inch |

### 4C. Rim + Tyre Combos (Click & collect ONLY — fitment included)

#### Quantum Rim + Tyre Combo — status: active
Tags: combo, taxi-combo, quantum, np350, hiace, 195-14c
Includes: 195/14C tyres x4 + 6/139/14 rims x4 + fitment at BBT Tembisa

| Variant | Price |
|---------|-------|
| Import WSW Tyres | R7,800 |
| LMC / Linglong Tyres (upgrade) | R8,600 |

#### 7-Seater Rim + Tyre Combo — status: active
Tags: combo, 7-seater-combo, avanza, rumion, ertiga, 7-seater, 185-70-14
Includes: 185/70/14 WSW tyres x4 + 14-inch rims x4 + fitment

**CRITICAL — bolt pattern warning (must appear in description):**
- 5x114 = Toyota Rumion, Suzuki Ertiga
- 4x114 = Toyota Avanza
Wrong bolt pattern = rims will not fit. Always confirm before ordering.

| Variant | Price |
|---------|-------|
| Black Rims — Rumion/Ertiga (5x114) | R7,650 |
| Black Rims — Avanza (4x114) | R7,650 |
| Chrome Rims — Rumion/Ertiga (5x114) | R9,600 |
| Chrome Rims — Avanza (4x114) | R9,600 |

### 4D. NGK Spark Plugs — status: active
Tags: ngk, spark-plugs, service-part
One parent, vehicle fitment as variant. Part number in variant label.

| Variant | Part number | Price |
|---------|------------|-------|
| Toyota Quantum — set of 4 | LFR6C-11 | R200 |
| Suzuki Ertiga — set of 4 | KR6A-10 | R440 |
| Renault Kwid — set of 3 | LZKAR7A | R450 |
| Hyundai i10 — set of 3 | LKR6D-10E | R360 |
| Kia Picanto — set of 3 | LKR6D-10E | R360 |

### 4E. Oils & Fluids — status: active
Tags: engine-oil, oil, lubricant + brand tag
Shipping: nationwide, free over R500

| Product | Variant | Price |
|---------|---------|-------|
| Shell 15W-40 Engine Oil | 500ml | R50 |
| Shell 15W-40 Engine Oil | 5L | R400 |
| Liqui-Moly (arriving week 2) | TBC grades | TBC |

### 4F. Service Kits
#### Suzuki Ertiga Service Kit — status: active
Price: R975 | Tags: service-kit, ertiga, 7-seater
Includes: engine oil + oil filter + air filter | Fitment: Suzuki Ertiga 1.5 all years

#### Draft service kits (status: draft — activate when prices confirmed)
- Toyota Quantum Service Kit — R800
- VW Polo Vivo 1.4 Service Kit — R750
- Toyota Hilux 2.8 GD6 Service Kit — R950

### 4G. Car Accessories — all status: active
Tags: accessory + specific tag | Shipping: free over R500, R80 below

| Product | Price | Tags |
|---------|-------|------|
| Dash Camera Full HD 1080P | R850 | accessory, dash-cam, gadget, security |
| Leatherette Seat Covers 9-piece | R850 | accessory, seat-covers, interior |
| Steering Wheel Cover Leather Feel | R280 | accessory, steering-wheel, interior |
| All-Weather Rubber Floor Mats | R450 | accessory, floor-mats, interior |
| Foldable Reflective Car Sunshade | R180 | accessory |
| Steering Wheel Lock Anti-Theft | R380 | accessory, security |
| OBD2 Bluetooth Diagnostic Scanner | R450 | accessory, obd2, gadget |
| Jump Starter + Power Bank Combo | R1,200 | accessory, gadget, jump-starter |
| Reverse Camera Universal | R450 | accessory, gadget |
| Car Alarm System Basic | R650 | accessory, security |
| Microfibre Cloth Set 10-pack | R180 | accessory, car-care |
| Battery Terminal Clamps | R85 | accessory, battery |
| Tyre Puncture Repair Spray | R180 | accessory, tyre, safety |

### 4H. LED Headlight Globes — status: active
Tags: accessory, led, lighting, headlight

#### C6 LED Globe Set
| Variant | Price |
|---------|-------|
| H4 pair — Quantum, Hilux, older SA cars | R170 |
| H7 pair — Polo Vivo, Golf, modern cars | R120 |
| H11 pair | R120 |
| H3 pair | R120 |
| 9006 pair | R120 |

#### C12 LED Globe Set (premium)
| Variant | Price |
|---------|-------|
| H4 pair | R220 |
| H11 pair | R170 |

---

## 5. SHIPPING PROFILES (3 required)

| Profile name | Assigned to | Rates |
|-------------|------------|-------|
| Batteries | Osaka, Exide products | Click & collect FREE · Local 10km R80 · No nationwide |
| Tyres | All tyre products | Click & collect FREE · Local R80/tyre · Nationwide R120/tyre |
| Combos — Collect Only | Quantum combo, 7-Seater combo | Click & collect FREE only — no delivery |
| Accessories & Oils | Everything else | Click & collect FREE · Under R500: R80 · Over R500: FREE |

---

## 6. DISCOUNT CODES

| Code | Type | Value | Applies to |
|------|------|-------|-----------|
| TRADE250 | Fixed amount | R250 off | Products tagged "osaka" + "battery" |
| TRADE475 | Fixed amount | R475 off | Products tagged "exide" + "battery" |

Staff apply these codes at the counter when customer brings old battery for trade-in.
These codes are NEVER promoted online — in-store use only.

---

## 7. HOMEPAGE SECTION ORDER

Build these sections in this exact order (top to bottom):

1. Announcement bar — scrolling gold ticker
2. Navigation bar — BBT logo left, location centre, search + cart right
3. Hero section — headline + vehicle CTA + WhatsApp CTA + Spin & Win teaser
4. Trust strip — 4 badges (Google reviews, fitment, same-day, Peach Payments)
5. Shop by vehicle — horizontal scroll tiles (Taxi, 7-Seater, Passenger, Workshop)
6. Flash sale countdown — timer + featured product
7. Hot Combos — horizontal product scroll
8. Battery banner — full-width dark CTA card
9. Accessories scroll — horizontal product cards
10. Google Reviews strip — 3 review cards + link to Google
11. Loyalty points bar — Smile.io Bronze/Silver/Gold progress
12. WhatsApp sticky CTA — full-width green banner
13. Footer — 4 columns + social icons + payment icons
14. Mobile bottom nav — 5 items fixed to bottom (mobile only)

---

## 8. SEO SETTINGS

### Homepage
- Title: "Taxi Tyres, Car Batteries & Rim Combos Tembisa | Better Battery Tyres"
- Meta: "Quantum rim & tyre combos, Osaka & Exide batteries, passenger tyres — all in stock at BBT Tembisa & Midrand. WhatsApp 063 500 1740 for same-day fitment."

### Schema markup — add to layout/theme.liquid inside <head>
```html
<meta name="google-site-verification"
  content="nplCOZ8VDe2BoODUA4JFnoDZdsZL0LiVjm9bJzU3wfM" />

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "AutoPartsStore",
  "name": "Better Battery Tyres",
  "url": "https://www.betterbattery.co.za",
  "telephone": "063 500 1740",
  "email": "hello@betterbattery.co.za",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "140 Modderfontein Road",
    "addressLocality": "Tembisa",
    "addressRegion": "Gauteng",
    "postalCode": "1632",
    "addressCountry": "ZA"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "5.0",
    "reviewCount": "24"
  }
}
</script>
```

---

## 9. 301 REDIRECTS (enter before DNS switch)

Enter in Shopify Admin → Online Store → Navigation → URL Redirects:

```
/motor-spares                                       → /collections/service-kits
/tyres-1                                            → /collections/taxi-minibus
/tyres                                              → /collections/passenger-cars
/carbatteries                                       → /collections/passenger-cars
/accessories                                        → /collections/car-accessories
/instore                                            → /pages/instore-specials
/lubricants                                         → /collections/oils-fluids
/shop-1                                             → /collections/car-accessories
/product-page/quantum-14-combo                      → /products/quantum-rim-tyre-combo
/product-page/chrome-combo                          → /products/7-seater-rim-tyre-combo
/product-page/powertrac-195-14c-wsw                 → /products/195-14c-tyre
/product-page/powertrac-185-70-14-wsw               → /products/185-70-14-tyre
/product-page/powertrac-195-15c-wsw                 → /products/195-15c-tyre
/product-page/supavolt-619                          → /products/exide-eco-car-battery
/product-page/supavolt-646                          → /products/osaka-car-battery
/category/combo-deals                               → /collections/7-seater
/category/service-kits                              → /collections/service-kits
/category/all-products                              → /collections/all
/about-us                                           → /pages/about
/reviews                                            → /pages/reviews
/gallery                                            → /pages/gallery
/contact-8                                          → /pages/contact
/post/car-essentials-battery-tyres-accessories-more → /blogs/news/car-essentials-battery-tyres-accessories
```

**DO NOT switch DNS until all redirects are entered and verified.**
**DO NOT take the Wix site down until DNS has fully propagated (24–48 hours).**

---

## 10. GAMIFICATION APPS

| Feature | App | Status |
|---------|-----|--------|
| Spin & Win popup | WheelOfPopups (Shopify App Store) | Install at build |
| Flash sale countdown | Shopify native timer section | Built into theme |
| Loyalty points | Smile.io (free tier) | Install at build |
| Referral programme | Smile.io built-in | Enable at launch |
| Post-purchase scratch card | Klaviyo email automation | Phase 2 |

---

## 11. SOCIAL PROOF

- **Judge.me** — install from Shopify App Store, style to dark theme (#1D1D1D cards, #F5C000 stars)
- **Seed reviews** — import 6 Google reviews into Judge.me at build (one per hero product)
- **Review request** — Ntombi sends WhatsApp 24hrs after collection: g.page/r/CURQ3dL5N-RjEBM/review
- **Google reviews widget** — homepage strip showing 3 reviews, links to full Google profile

---

## 12. DAILY OPERATIONS VIA CLAUDE CODE CLI

Common commands Muneer uses to manage BBT via Claude Code CLI:

```bash
# Morning pulse
"give me today's BBT business pulse"

# Pricing
"update the [product] price to R[amount]"
"sync all prices from Google Sheet to Shopify"
"publish all draft products that now have confirmed prices"

# Orders
"show me all unfulfilled orders"
"mark order #[number] as fulfilled — customer collected"

# Marketing
"write this week's Friday flash sale WhatsApp broadcast"
"write a TikTok script for the [product] — 30 seconds"
"plan next week's content calendar"

# B2B
"show me all workshop prospects not yet contacted"
"write a WhatsApp intro for [workshop name] in [area]"
```

---

## 13. THEME COMMANDS

```bash
# Start local dev server (hot-reload against live store)
shopify theme dev

# Lint all Liquid files
shopify theme check

# Push theme to store
shopify theme push

# Pull latest theme from store
shopify theme pull
```

Theme Check config: `.theme-check.yml` (extends `theme-check:recommended`)

---

## 14. THEME ARCHITECTURE

This is a **Shopify Dawn Theme** — Shopify's flagship free theme.

### Data flow
```
layout/theme.liquid          ← single HTML shell for all pages
  └─ sections 'header-group' ← sticky header section group
  └─ content_for_layout      ← renders the matched template
  └─ sections 'footer-group' ← footer section group
templates/*.json             ← declare which sections appear on each page type
sections/*.liquid            ← full-width modules with settings + optional blocks
blocks/*.liquid              ← nestable sub-components rendered inside sections
snippets/*.liquid            ← reusable fragments (no schema, no merchant settings)
```

### CSS variables / theming
Global theme settings defined in `config/settings_schema.json` and rendered as CSS
custom properties on `:root` via `snippets/css-variables.liquid` inlined in `<head>`.
BBT brand variables (--bbt-gold, --bbt-black etc.) are added to this file.
Above-the-fold base styles in `assets/critical.css` — everything else in
component-scoped `{% stylesheet %}` tags.

### Schema settings → CSS pattern
- **Single CSS property** → emit inline CSS variable, consume with `var(--name)`
- **Multiple CSS properties** → emit as BEM modifier class, style in `{% stylesheet %}`

### Localization
Schema label strings use `t:` keys resolving from `locales/en.default.schema.json`.

### `{% stylesheet %}` / `{% javascript %}` tags
Shopify deduplicates these across includes — safe to put component CSS/JS directly
in section and block files.

### `templates/*.json` files
Auto-generated by Shopify admin. Use `shopify theme pull` to sync. Avoid hand-editing
section IDs directly.