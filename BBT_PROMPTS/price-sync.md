# BBT Price Sync — Google Sheets to Shopify

Run whenever cost prices change or new supplier quotes received.

## Instructions

STEP 1 — READ GOOGLE SHEETS
Connect to Google Sheets MCP.
Read the master price list:
https://docs.google.com/spreadsheets/d/1-qFbLw03iqz6o6RE2XscF1Kq5r44WTNsoJCv0vV7Oko

Extract for each product:
- Product name
- Variant/size
- Cost price
- Current selling price
- Current GP%

STEP 2 — CALCULATE NEW PRICES
For any product where cost price has changed:
- Recalculate selling price to maintain target GP%
- Check against GP floor (OPERATIONS.md section 1)
- Flag any product where GP floor cannot be maintained
  at current market price — escalate to Muneer

STEP 3 — COMPARE TO SHOPIFY
Query current Shopify prices for same products.
List all products where price needs updating.
Show: current Shopify price vs new calculated price.
Get Muneer approval before making any changes.

STEP 4 — UPDATE SHOPIFY (after approval)
Use shopify store execute to update variant prices.
Update compare-at prices proportionally.
Never remove compare-at prices.
Never update battery compare-at prices.

STEP 5 — CONFIRM
List all products updated with old and new prices.
Calculate average GP% before and after.
Flag any products still below GP floor.
