# BBT Add New Product

Use this template whenever adding any new product to BBT.

## Required information (collect before starting)
- Product name and brand
- Category (batteries/tyres/combos/accessories/oils/service-kits)
- Cost price (from supplier invoice)
- Target GP% (see OPERATIONS.md for minimums by category)
- Variants (sizes, colours, specs)
- Fitment vehicles (if applicable)
- Stock quantity
- Supplier name

## Instructions

STEP 1 — CALCULATE PRICING
- Selling price = cost price ÷ (1 - target GP%)
- Compare-at price = selling price × 1.15
- Round to nearest R10
- Confirm GP floor from OPERATIONS.md is met
- Never price below GP floor under any circumstances

STEP 2 — DETERMINE TAGS
Based on category and fitment, assign correct tags so
automated collection rules work:
- Battery products: battery + brand tag + vehicle tags
- Tyre products: tyre + size tag + vehicle tags
- Accessories: accessory + specific category tag
- Oils: engine-oil + brand tag
- Service kits: service-kit + vehicle tag

STEP 3 — CREATE IN SHOPIFY
Use shopify store execute to create the product with:
- Correct title format: [Brand] [Spec] [Type] — [Fitment]
- Full description with fitment, specs, WhatsApp CTA
- All variants with correct prices and compare-at
- Correct tags for automated collection sorting
- Status: active if confirmed in stock, draft if pending

STEP 4 — VERIFY
- Product appears in correct collection automatically
- Price displays correctly on product page
- Variants selectable on product page
- WhatsApp CTA present in description

STEP 5 — COMMIT
- No git changes needed (store data not theme code)
- Confirm product URL is live
- Report: product name, collection, price, GP%
