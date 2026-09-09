# SOP, Returns and condition spike
Owner: Puneet, until delegated
Trigger: **3 or more condition complaints on the same SKU within 7 days**, OR **2 or more complaints from the same city within 5 days**, OR any single complaint about a product that arrived unsafe to eat. A refund request counts as a complaint whether or not the customer asks for money back.
First time vs steady state: the first run takes about two hours because you are building the batch trace. Once batch codes are being recorded at dispatch, later runs take about 40 minutes.

## When to use this
Condition on arrival has failed for more than one customer in a short window. In this brand, every negative review on record is about condition or transit, never about taste, so this is the SOP that covers essentially all of the quality risk.

## The playbook

1. **Confirm it is a cluster, not a coincidence. 15 minutes.** Pull every complaint on that SKU for the last 14 days. Write down city, ship date, courier and, if you have it, batch. Two complaints from one city on one courier is a cluster. Two complaints from two cities a week apart is not.

2. **Stop the bleeding on that lane, not the whole product. 10 minutes.** If the pattern is one city or one courier, hold shipments on that lane only. Pulling a SKU nationally because Delhi failed costs more than the returns do.

3. **Check the standing seasonal risk first.** The known failure mode is heat on Almond Delight and Dry Fruit Meetha Paan into Delhi, Hyderabad and Lucknow between May and August. If the cluster is inside that window and those cities, you already know the cause, skip to step 5 and ship insulated.

4. **Trace the batch. 30 minutes.** Same production day, same input lot, same packer. If the answer is yes, this is a vendor or process issue and step 6 applies. If the answer is no, it is transit.

5. **Reply to every affected customer within the day.** Use `templates/returns-quality-apology.md`. Refund the affected portion without making them ask twice. The precedent is already set and it worked: the customer who reported melted edges was refunded, told the truth about a known weak spot, and said they would reorder in October.

6. **Escalate to the vendor if the trace points there. 20 minutes.** Use the batch reject template when it exists. Name the batch, the date, the defect and the quantity affected. Attach photographs from the customer, with any personal detail cropped out.

7. **Freeze the listing only if the defect is a safety issue.** Melted edges is a quality issue, so keep selling and fix the lane. An allergen or contamination issue is a safety issue, so pull the listing on every channel first and ask questions second.

8. **Write the fix into the product page, not just the SOP. 15 minutes.** The insulated summer box is already free and already mentioned in the order notes flow. If customers are still hitting the problem, the offer is not visible enough. Move it up the page.

9. **Log it. 5 minutes.** SKU, dates, city, courier, batch, count, cause, cost. Five of these lines will tell you whether you have a courier problem or a kitchen problem.

## Decision points

**Refund, replace, or both.** Refund the affected portion by default because it is faster and it ends the thread. Replace only when the customer asks, or when the order was a gift and the recipient never got a usable box. A failed gift is a lost referral, and the referral is worth more than the box.

**Whether to tell customers before they notice.** If the cluster is a whole batch or a whole lane, message everyone on that lane before they open the box. This brand already admits weakness in plain words and it earns trust every time.

**When to change courier.** One bad week is not a courier decision. Two clusters on the same courier in a season is.

## Templates this uses
- `my-work/ops-manager/templates/returns-quality-apology.md`
- Batch reject vendor email, not yet written. Ask for the full vendor kit.

## When to escalate
Call the founder immediately for anything involving an allergen, foreign matter, or a customer reporting illness. Do not run the rest of this SOP first. Same for any complaint that arrives publicly on a marketplace listing during the festival window, because the placement damage outruns the refund.

## Done
- [ ] Cluster confirmed or ruled out, in writing
- [ ] Affected lane held, or ruled out
- [ ] Every affected customer answered and refunded the same day
- [ ] Cause recorded as vendor, kitchen or transit
- [ ] Log line written
