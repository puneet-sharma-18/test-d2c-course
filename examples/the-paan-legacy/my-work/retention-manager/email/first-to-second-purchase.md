# Email, First to second purchase
Fires: **21 days after a first order**, with no second order placed.
Segment: `first-time-buyers`, 21 days in.
Tone: this is the one with room for the story. Still short. The story is three sentences, not a page.
Personalisation tokens: {first_name}, {first_product}, {reorder_link}, {meetha_link}

## Subject lines
1. {first_name}, what usually happens next
2. The paan most people buy second
3. Three weeks in

## Body

> Hi {first_name},
>
> You bought {first_product} three weeks ago. Nothing to do here, this is just the thing I would tell you if you were standing in the shop.
>
> I sold my family's paan shop in Kanpur to start this, because the shop had stopped making the version I grew up with. The category traded a two thousand year old after-meal habit for a tobacco hit and a stain on the wall. So we make the one your grandmother would still recognise. Rolled by hand, named ingredients, nothing to spit out.
>
> **What usually happens next.** Most people who start with us buy a second thing within about six weeks, and it is usually not the same one. People who start on Granola Goodness end up on the Meetha Paan. People who start on the Meetha Paan end up sending the Almond Delight to their in-laws.
>
> If you want the ₹179 entry one, it is here: {meetha_link}
> If you want what you had again: {reorder_link}
>
> And if the first box was not right, reply and tell me. That is more useful to me than a second order.
>
> Puneet
> The Paan Legacy
>
> {unsubscribe_link}

## The one CTA
{meetha_link}, the ₹179 entry SKU. The second link is a convenience, not the ask. The brand's house move is to downsell to the cheaper product, and this email does that rather than pushing the ₹299 box.

## When not to send
- A second order already placed. Check at send, not at schedule.
- Open complaint or refund on the first order
- The first order was itself a gift sent to someone else, where the buyer may never have tasted it. The story lands wrong.
- No marketing consent

## Compliance
Marketing email. Consent required, unsubscribe link mandatory under the DPDP Act. No claim beyond "after-meal habit", which sits inside the claim wall.

## Source
`my-work/voice-of-customer/2026-09-09-voc-report.md`, theme 7 and the first-to-repeat section. The crossover claim is real and directional: two documented cases of granola to paan and none in reverse. The founder story is from `CLAUDE.md` Sections 1 and 3.

## SAFETY FLAGS
1. **"Most people who start with us buy a second thing within about six weeks"** rests on the same single customer as the replenishment timing, and it is stated here as if it were a pattern. It is not, it is n=1. **Either soften it to "some people" or get the real cohort number first.** This line blocks the email as written.
2. **"People who start on Granola Goodness end up on the Meetha Paan"** is 2 of 27 messages. Directionally consistent, both in the same direction, but thin. Acceptable as a soft claim, flagged so you know its weight.
3. The two thousand year figure is inherited from the brand's own live product page and ad copy. Not independently sourced.
