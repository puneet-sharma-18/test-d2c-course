# WhatsApp, Replenishment
Fires: **35 days after delivery**, with no second order in between. That is the six week reorder gap minus seven days.
Segment: `first-time-buyers` on their first order, `repeat-buyers` on any later one. Both receive the same message.
Tone: a reminder, not an offer. No discount. No urgency.
Personalisation tokens: {first_name}, {product}, {reorder_link}

## Body

> Hi {first_name}, Puneet. You bought {product} about five weeks ago.
> If it runs out around now, here is the link so you do not have to go looking: {reorder_link}
> No subscription, no saved card, no auto-payment. I just ping you.
> If the timing is wrong, tell me and I will change it or stop.

## The one CTA
{reorder_link}, straight to a prefilled cart of the last order.

## When not to send
- A second order was placed after the first. The trigger checks this at send time, not at schedule time.
- Open complaint or unresolved refund
- Customer asked to stop these
- No WhatsApp marketing opt-in
- **The product is out of stock.** Reminding someone to reorder something they cannot buy is the fastest way to lose the opt-in. Check inventory at send.

## Compliance
WhatsApp category: **Marketing**. Needs marketing opt-in and template approval, and it counts against Meta's per-user marketing message limits. The stop instruction in the last line is doing compliance work, do not cut it for length.

## Source
This is not invented. It is the flow the founder already ran by hand and already got a yes on. From `my-work/voice-of-customer/2026-09-09-voc-report.md`, theme 8, a three-time buyer wrote "Need a subscribe-and-save. Reordering manually every six weeks is annoying." The founder replied offering "a calendar reminder, I add you to a list and ping you 5 days before the 6-week mark with a one-click reorder. No subscription friction, no auto-payment." The customer replied YES within two minutes. The wording above is that offer, made into a template.

## SAFETY FLAGS
1. **The six week window rests on one customer.** n=1. It is the only cadence figure that exists anywhere in the brand's files, and the founder's own unit economics assume 1.6 orders a year, which is roughly a 33 week gap, not six. Those two numbers cannot both be right. **Run this at 35 days for one cohort and measure before rolling it out**, because if the real gap is longer this template arrives months early and trains people to ignore you.
2. **No discount, deliberately.** The brand's anti-positioning says never compete on price. Most replenishment templates lean on a percentage off and this one cannot. If someone adds `{discount_value}` to this template later, it breaks Section 3 of the brand profile.
