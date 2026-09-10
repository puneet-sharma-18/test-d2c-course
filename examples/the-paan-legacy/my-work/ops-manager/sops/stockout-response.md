# SOP, Stockout response
Owner: Puneet, until delegated
Trigger: Any SKU whose on-hand cover falls below **14 days** at the trailing 28 day sell rate. Between **15 September and 8 November**, the trigger tightens to **21 days** for Almond Delight and Dry Fruit Meetha Paan, because the corporate Diwali bundle consumes both at once.
First time vs steady state: the first run takes about 90 minutes, most of it spent establishing a real cover number per SKU. Once that number is on a sheet the founder trusts, every later run is about 25 minutes.

## When to use this
A gifting SKU is going to run out before the next production batch lands. Use it the moment the trigger fires, not when the shelf is empty. The whole point is to act while there is still stock to allocate.

## The playbook

1. **Get a real cover number. 20 minutes, first run only.** The product export in the brand profile is flagged as a partial pull, so the sell rate in it understates reality, possibly by a lot. Pull total units sold per SKU across the site, Zomato and Swiggy for the last 28 days, divide on-hand by the daily rate, and write the result somewhere permanent. Until this exists, every step below is running on a guess.

2. **Rank what is left by contribution, not by units. 10 minutes.** Contribution after commission and shipping is 38 to 42% on the site and 28 to 32% on marketplace. The same box is worth meaningfully more sold direct. When stock is short, the site gets it.

3. **Decide the allocation. Founder decision, see decision points.** Options are: hold stock for corporate and gifting, keep marketplace listings live, or throttle paid spend on the affected SKU.

4. **Throttle the ads before the site. 10 minutes.** Paying to send traffic to a product you cannot ship is the most expensive mistake in this whole SOP. Pause or cap the ad set for that SKU first. The heritage ritual creative on Almond Delight is the best performing one in the account, so pause it reluctantly and last, but pause it.

5. **Update the product page. 5 minutes.** Use `templates/stockout-page-note.md`. Give a real restock date or no date at all. A vague "back soon" generates a support thread per customer.

6. **Message recent buyers who have an order in flight. 15 minutes.** Only those affected. Use `templates/stockout-apology-recent-buyers.md`.

7. **Place or escalate the replenishment order. 20 minutes.** Use `vendor-kit/purchase-order-confirmation.md`. Pin quantity, unit price, delivery date and quality spec in writing. Saffron moved in April and granola has a single-vendor bottleneck, so neither price nor date is safe to assume.

8. **Offer the honest downsell. Ongoing.** If Almond Delight is out, Meetha Paan at ₹179 is the entry into the same ritual. This is already how the brand talks. It is not a consolation prize, it is the house recommendation.

9. **Log it. 5 minutes.** One line: SKU, date the trigger fired, cause, days out of stock, revenue missed. Three of these lines tell you whether the problem is forecasting or the vendor.

## Decision points

**Who gets the last stock.** Corporate and gifting orders are pre-committed, higher basket and carry a deadline that cannot move. Ordinary site orders are worth more per unit than marketplace. Suggested order of priority: confirmed corporate first, site second, marketplace last. The founder overrides this whenever a corporate account is at risk.

**Whether to delist on marketplace or go out of stock naturally.** Going out of stock on Zomato or Swiggy affects placement. Delisting deliberately is cleaner but has to be reversed by hand. Below 7 days of cover, delist.

**Whether to keep taking orders with a longer ship date.** Only if the vendor has confirmed a date in writing. Never on a verbal.

## Templates this uses
- `my-work/ops-manager/templates/stockout-page-note.md`
- `my-work/ops-manager/templates/stockout-apology-recent-buyers.md`
- `my-work/ops-manager/vendor-kit/purchase-order-confirmation.md`

## When to escalate
Stop following this SOP and call the founder when any of these is true: a confirmed corporate order cannot be fulfilled on its committed date, the vendor cannot give a written delivery date, or two or more SKUs breach the trigger in the same week. Any of those is a production capacity problem, not a stock problem, and the play is different.

## Done
- [ ] Real cover number recorded for every SKU
- [ ] Ads for the affected SKU paused or capped
- [ ] Product page carries a real date or no date
- [ ] Affected in-flight customers messaged
- [ ] Replenishment order confirmed in writing, with a date
