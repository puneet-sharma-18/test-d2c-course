# Segment, Repeat buyers

## Definition, as a runnable filter

```
lifetime_order_count >= 2
AND last_order_date >= today - 180 days
AND marketing_consent_email == true OR marketing_consent_whatsapp == true
AND open_complaint == false
```

Two sub-states matter, and they take different messages:

**Active.** `last_order_date >= today - 60 days`. Gets replenishment only.

**Gone quiet.** `last_order_date < today - 60 days AND last_order_date >= today - 180 days`. Gets the win-back pair.

Past 180 days quiet, stop. That is a lapsed list, not a retention segment, and mailing it is how you burn a sender reputation.

## Size estimate

**No data**, for the same reason as the other segment file. The store connection points at a different brand.

The only real figure available: repeat purchase rate of **30%**, from the founder's 2026-05-12 record, independently corroborated by the customer research where **8 of 27 customers showed a documented second purchase**. Two independent sources landing on the same number is the strongest data point in this whole repo, which is why it is worth protecting.

## What this segment actually cares about

Two different things, because there are two personas inside it.

**The ritual restorer** stays for the calendar. Sunday lunch, evening after a meal. Their persona card says what would bring them back is "nothing extra, it is already a fixed slot in the week". So do not sell to them. Just be reachable when the box empties.

**The gifter** is seasonal, not weekly. Their card says what would bring them back is "the festival calendar, and there is no mechanism holding them between festivals". That gap is the whole opportunity in this segment.

And one behaviour worth designing around: **repeat buyers here broaden rather than deepen.** Three of the eight documented repeat customers bought a *different* SKU the second time, not more of the same. "I bought this because I was bored of meetha paan. Now I rotate between the two." The range is doing the retention work, so a replenishment message that only ever offers the same box is under-serving them.

## Templates that fire for them

| Template | When |
|---|---|
| `whatsapp/order-confirmation.md` | On payment |
| `email/order-confirmation.md` | On payment |
| `whatsapp/delivery-check-in.md` | 3 days after delivery |
| `whatsapp/replenishment.md` | 35 days after delivery, active sub-state |
| `whatsapp/win-back.md` | 60 days quiet |
| `email/win-back.md` | 62 days quiet, only if no WhatsApp reply |

## Retargeting audience

This is the segment worth excluding from prospecting, not just targeting. When the ad account comes back on, suppress it from cold campaigns. Paying acquisition prices to reach someone who already buys every six weeks is the most common way a returning account wastes its first month.

## The gap this segment exposes

There is no festival trigger in this run. The gifter half of this segment goes quiet between occasions and nothing reaches them, which their own persona card names as the problem. Diwali is 8 November. **A dated festival reminder to prior gifters is probably worth more than every other template here combined**, and it is not in the default five moments. Ask for it and it takes twenty minutes.
