# BBT Reorder Alert

Run weekly — every Monday with the weekly report.

## Instructions

STEP 1 — CHECK STOCK LEVELS
Query Shopify inventory for all active products.
Flag any product where:
- Quantity is below 5 units → URGENT reorder
- Quantity is below 10 units → reorder soon
- Quantity is zero → OUT OF STOCK — urgent

STEP 2 — SALES VELOCITY CHECK
For each flagged product, check units sold last 7 days.
Calculate days of stock remaining:
days remaining = current stock ÷ weekly sales rate

STEP 3 — PRIORITY REORDER LIST
Sort by urgency:
1. Out of stock — order immediately
2. Under 5 units with high sales velocity
3. Under 10 units with moderate sales velocity

STEP 4 — REORDER RECOMMENDATIONS
For each flagged product show:
- Product name and variant
- Current stock level
- Weekly sales rate
- Days of stock remaining
- Recommended reorder quantity (4 weeks of stock)
- Supplier (from CLAUDE.md supplier list)

STEP 5 — REPORT FORMAT
Present as a clean reorder list Muneer can action
immediately — WhatsApp to supplier or place order.
Flag anything that will run out before the weekend
(Friday flash sale risk) in CAPITALS.
