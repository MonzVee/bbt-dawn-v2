# BBT — Better Battery Tyres | Claude Code Context

## CRITICAL ARCHITECTURE RULE
Never hardcode products, prices, brands, SKUs, counts, 
or any data that changes over time into theme files, 
CLAUDE.md, or OPERATIONS.md.
- Products and prices → always query Shopify live
- Cost prices and GP → always read from Google Sheets
- Review counts → never hardcode, use dynamic copy only
- Supplier brands → treat as interchangeable, not fixed

---

## 1. BUSINESS IDENTITY

Trading name: Better Battery Tyres (BBT)
Location: 140 Modderfontein Road, Tembisa, Gauteng
WhatsApp: 063 500 1740
Email: hello@betterbattery.co.za
Website: betterbattery.co.za
Store: 01jkmb-hf.myshopify.com
Google Business: g.page/r/CURQ3dL5N-RjEBM/review

Operating hours:
- Monday to Friday: 08:00 - 17:00
- Saturday: 08:00 - 15:00
- Sunday: 09:00 - 12:30

---

## 2. BRAND DESIGN SYSTEM

### Colour palette (CSS variables — never hardcode hex in content)
--bbt-gold:    #F5C000  (primary — CTAs, prices, highlights)
--bbt-black:   #111111  (page background, navbar)
--bbt-dark:    #1D1D1D  (card backgrounds, surfaces)
--bbt-surface: #2A2A2A  (borders, dividers)
--bbt-cream:   #E8E0C8  (body text on dark)
--bbt-muted:   #888888  (secondary labels, captions)
--bbt-wa:      #25D366  (WhatsApp CTAs exclusively)
--bbt-red:     #E53935  (flash sale, urgency, badges)

### Design principles
- Dark theme throughout — #111111 background
- Mobile-first — all layouts designed for 390px viewport
- WhatsApp-first — WhatsApp CTA on every product page
- Native Dawn sections first — custom code only where 
  Dawn has no native solution
- No custom JavaScript — apps handle gamification
- No hardcoded content in theme files

### Typography
- Font: system font stack (-apple-system, BlinkMacSystemFont, 
  Segoe UI, Roboto, sans-serif)
- Prices: weight 800, --bbt-gold, minimum 18px
- Headings: weight 700
- All caps: section labels, badges, category names only

---

## 3. CUSTOMER SEGMENTS (priority order)

1. Taxi and minibus operators
   Vehicles: Toyota Quantum, NV350, HiAce
   Primary needs: tyres, rim combos, batteries, spark plugs

2. 7-seater Uber and Bolt drivers
   Vehicles: Toyota Avanza, Rumion, Suzuki Ertiga, 
   Renault Triber
   Primary needs: rim combos, tyres, batteries, service kits

3. Passenger car owners
   Vehicles: VW Polo Vivo, Toyota Hilux, Corolla, 
   Suzuki Swift, Hyundai i20, BMW, Audi, Mercedes
   Primary needs: batteries, tyres, accessories, oils

4. Independent workshops and mechanics (B2B)
   Primary needs: oils, batteries, consumables, spark plugs
   Terms: strictly COD, no accounts, no credit

---

## 4. PRODUCT ARCHITECTURE RULES

### Categories (current — will expand)
- Batteries (multiple brands and tiers — query Shopify live)
- Tyres (commercial and passenger — query Shopify live)
- Rim + Tyre Combos (vehicle-specific — query Shopify live)
- Spark Plugs (by vehicle fitment)
- Oils and Fluids (multiple brands and grades)
- Service Kits (by vehicle)
- Car Accessories (primary online growth category)
- LED Globes and Lighting

### Product architecture principles
- Brands are interchangeable — never lock to a specific 
  supplier brand in rules or theme code
- Variants = customer-facing options only (size, colour, 
  bolt pattern, tyre brand upgrade)
- Tags drive automated collection membership — always tag 
  correctly on product creation
- Status: active = confirmed in stock
  Status: draft = price TBC or stock unconfirmed

### Battery-specific rules
- Scrap deposit mechanic: customer pays full price online,
  receives trade-in credit at counter on collection
  (R amount varies by brand — check product description,
  never hardcode amount in theme)
- Pro-rata warranty: period varies by brand — check 
  product description, never hardcode in theme
- Batteries NEVER discounted — no exceptions
- Battery prices never appear in flash sales or promotions

### Combo-specific rules
- Always include fitment note in description
- Bolt pattern warning mandatory on all combos
- Ship nationwide at flat courier fee (check shipping 
  profile for current rate — never hardcode in theme)
- Tyre brand upgrade option (e.g. Linglong) modeled 
  as 3rd variant option "Tyre Brand"

### Accessories rules
- Primary online revenue growth category
- Target: top 150 automotive SKUs online in SA
- High margin category — price confidently
- Ships nationwide (check current shipping profile rate)
- Compare-at price always set to show savings

---

## 5. COLLECTION ARCHITECTURE

Collections are driven by automated tag rules.
Never hardcode collection membership — tags handle it.

Current collection handles:
- taxi-minibus
- 7-seater
- passenger-cars
- service-kits
- oils-fluids
- car-accessories
- workshop-trade (manual — landing page only)
- batteries (utility — tag: battery)
- combos (utility — tag: combo)
- flash-sale (utility — tag: flash-sale)

Tag rules: query Shopify live for current rules.
Never hardcode tag lists in CLAUDE.md.

---

## 6. PRICING RULES

### GP floors by category (minimums — never go below)
| Category | Minimum GP | Target GP |
|----------|-----------|-----------|
| Batteries | 25% | 28% |
| Tyres | 25% | 30% |
| Combos | 30% | 38% |
| Oils and Fluids | 30% | 40% |
| Service Kits | 35% | 45% |
| Car Accessories | 40% | 55% |
| LED and Lighting | 45% | 60% |

### Pricing strategy
- Google Sheets is the single source of truth for cost prices
- Shopify holds live selling prices
- Never sync prices without checking GP floor first
- List accessories at confident margins — customers 
  have no price anchor on accessories
- Batteries and tyres have known market prices — 
  price competitively but never below GP floor

### Never discount
- Batteries — under any circumstances, any brand
- Any product below GP floor
- Combos below 30% GP

### Flash sale rules
- Feature accessories or high-margin products only
- Never feature batteries
- Tag product with flash-sale in Shopify Admin
- Remove tag to end sale — theme updates automatically
- Always maintain GP floor even on sale price

---

## 7. SHIPPING POLICY

All rates are managed in Shopify shipping profiles.
Never hardcode rates in theme files or copy.
Query shipping profiles for current rates.

Current policy (as at launch):
- All products ship nationwide
- Batteries: flat fee per order
- Tyres: flat fee per tyre
- Combos: flat fee via Pudo nationwide + free collect
- Accessories and Oils: flat fee per order
- Free click and collect: always available at Tembisa store

No free delivery threshold on any product category.
Free delivery may be introduced as a promotional 
mechanic in future — update shipping profiles when ready,
never hardcode in theme.

---

## 8. WORKSHOP TRADE (B2B)

### Current policy
- Strictly COD — no accounts, no credit, no exceptions
- Best market prices — no formal discount structure
- WhatsApp 063 500 1740 as primary contact
- Workshop Trade page: /pages/workshop-trade

### Future B2B features (on the horizon)
- Purchase history-based loyalty pricing after 
  several months of trading data
- WhatsApp enquiry flow for bulk pricing
- Online trade application form (business details capture)
- These features require Muneer's explicit approval 
  before implementation

---

## 9. WHATSAPP OPERATIONS

### Primary number: 063 500 1740
- All customer enquiries
- Order confirmations
- Delivery coordination
- Workshop trade enquiries

### WhatsApp link format (always pre-fill product context)
Product pages: 
https://wa.me/27635001740?text=Hi%20BBT%2C%20I%27m%20interested%20in%3A%20[product]

Generic (homepage, footer, banners):
https://wa.me/27635001740

### Broadcast schedule
- Friday 15:30: launch flash sale broadcast
- Saturday 09:00: follow-up broadcast
- Sunday 17:30: close sale broadcast
- All broadcasts require Muneer approval before sending

### Automation (future)
- Ntombi AI agent — Meta Business Agent on primary number
- ManyChat — new dedicated number for CTWA ad traffic
- Dondy — abandoned cart WhatsApp recovery (installed)
- These are future activations — not yet live at launch

---

## 10. CHANNEL EXPANSION ROADMAP

### Live at launch
- Shopify (betterbattery.co.za)
- WhatsApp broadcast (manual)
- Google Business Profile
- TikTok, Instagram, Facebook (organic)

### Month 1-2 post launch
- WhatsApp automation (Ntombi / Meta Business Agent)
- ManyChat CTWA automation (new number)
- Dondy abandoned cart recovery
- Top 150 automotive SKU research and catalogue expansion
- Google Shopping activation

### Month 2-3
- Takealot seller account
- First Takealot listings (accessories first)

### Month 3-4
- Makro marketplace
- Wherehouse (multi-channel management — review when 
  managing 3+ channels)

### Month 6+
- Amazon SA (when available)
- Investor partnership — three-tier product strategy 
  (budget / mid / premium across all categories)
- East Vaal Motors — OEM genuine parts online
- Wholesale to other fitment centres

---

## 11. HUMAN IN THE LOOP — ESCALATION RULES

Claude Code must ALWAYS get Muneer's approval before:
- Any price change on any product
- Creating or activating any discount or promotion
- Adding any new product to the live catalogue
- Sending any WhatsApp broadcast
- Publishing any theme change to the live store
- Processing any refund over R500
- Changing any shipping profile or rate
- Any B2B pricing or discount decision

Claude Code may act without approval on:
- Querying store data (read-only operations)
- Writing draft content for review
- Running theme check
- Committing to git (not pushing to live store)
- Reporting and analysis

---

## 12. DATA SOURCES (single source of truth)

| Data type | Source | Never use |
|-----------|--------|-----------|
| Product prices | Shopify (live query) | CLAUDE.md |
| Cost prices and GP | Google Sheets | CLAUDE.md |
| Stock levels | Shopify inventory | CLAUDE.md |
| Review counts | Google Business (ask Muneer) | Hardcoded |
| Shipping rates | Shopify shipping profiles | CLAUDE.md |
| Business rules | CLAUDE.md + OPERATIONS.md | Shopify metafields |
| Broadcast copy | OPERATIONS.md prompts | Hardcoded in theme |

---

## 13. THEME ARCHITECTURE

Theme: Shopify Dawn (native-first)
Repo: github.com/MonzVee/bbt-dawn-v2
Store theme ID: 149190541414 (unpublished — v2)
Live theme: BBT Dawn v1 (password protected during build)

### Architecture principles
1. Native Dawn sections first
2. Custom sections = HTML + CSS only, zero custom JS
3. All colours via CSS variables
4. Apps handle gamification (Spin & Win, countdown timer)
5. No hardcoded content in theme files
6. No hardcoded prices, counts, or rates anywhere

### Key files
- layout/theme.liquid: GSC tag, schema markup, CSS vars, 
  mobile bottom nav
- config/settings_data.json: BBT colour scheme defaults
- sections/bbt-*.liquid: custom BBT homepage sections
- templates/*.json: page template assignments
- CLAUDE.md: business rules (this file)
- OPERATIONS.md: weekly operating procedures
- BBT_PROMPTS/: reusable operational prompts

### Theme commands
shopify theme push --theme=149190541414 --store=01jkmb-hf.myshopify.com
shopify theme check
shopify store auth (for Admin API operations)

### Google Search Console verification
Tag is already in layout/theme.liquid.
Property: betterbattery.co.za

### Local Business schema
Already in layout/theme.liquid.
Type: AutoPartsStore
Never update schema manually — edit theme.liquid only.

---

## 14. DAILY OPERATIONS (CLI commands)

Morning pulse:
"Give me today's BBT business pulse"

Price update:
"Update [product] price to R[amount] — confirme the details: 
[name, category, price, cost price, variants, tags]"

Flash sale setup:
"Set up this week's flash sale — feature [product], 
sale price R[amount], runs Friday 15:30 to Sunday 17:30"

Broadcast:
"Write this week's Friday broadcast — feature [product] 
at R[price], sale ends Sunday 17:30"

Weekly report:
"Give me last week's BBT performance report — 
revenue, top sellers, GP by category"

Reorder alert:
"Check stock levels — flag anything needing reorder"

---

IMPORTANT: This file contains business rules only.
Never use CLAUDE.md as a data source for products, 
prices, inventory, or any data that changes.
Always query Shopify live or read Google Sheets 
for current data.
