# Segment, First-time buyers

## Definition, as a runnable filter

```
lifetime_order_count == 1
AND first_order_date >= today - 180 days
AND marketing_consent_email == true OR marketing_consent_whatsapp == true
AND open_complaint == false
```

Anyone past 180 days with one order is not a first-time buyer any more, they are a one-and-done. That is a different segment with a different message, and it is on the full run rather than this one.

## Size estimate

**No data.** The connected Shopify store is Anutilam Rice at anutilam.com, a different brand, and no data was read from it. Nothing in this repo carries a customer count.

What can be said from the founder's own May record: repeat purchase rate runs at 30%, independently corroborated at 8 of 27 in the customer research. So roughly **70% of customers in any period sit in this segment**. On a business doing about ₹30L a month at a ₹734 blended AOV, that is a meaningful number of people, but I am not going to multiply those two four month old figures together and present the result as a segment size.

## What this segment actually cares about

From the ritual restorer persona card. They bought to put an after-meal habit back on a table other people sit at. What worried them before paying was one thing: whether this is spit-out paan or eat-and-swallow. They have now answered that question themselves by eating it.

Which means **the job with this segment is not persuasion any more, it is timing.** They already know the product works. They need to be reachable when the box runs out.

## Templates that fire for them

| Template | When |
|---|---|
| `whatsapp/order-confirmation.md` | On payment |
| `email/order-confirmation.md` | On payment |
| `whatsapp/delivery-check-in.md` | 3 days after delivery |
| `whatsapp/replenishment.md` | 35 days after delivery |
| `email/first-to-second-purchase.md` | 21 days after first order |

Note the sequence: the email at day 21 carries the story, the WhatsApp at day 35 carries the reminder. If someone orders after day 21, the day 35 message must not fire.

## Retargeting audience

A Meta custom audience of this segment is worth building, but **note that the ad account has spent nothing for 22 days**, per `my-work/growth-analyst/2026-09-10-brief.md`. A retargeting audience with no campaign behind it does nothing. Build the audience when the account comes back on.
