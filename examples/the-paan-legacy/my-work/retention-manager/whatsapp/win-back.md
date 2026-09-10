# WhatsApp, Win-back
Fires: **60 days after the last delivery**, on a customer with **two or more lifetime orders**. Sent alongside the win-back email, WhatsApp first, email 48 hours later if there is no reply.
Segment: `repeat-buyers` who have gone quiet. See the segment file for the exact filter.
Tone: no guilt, no offer, no urgency. A note, not a campaign.
Personalisation tokens: {first_name}, {last_product}, {reorder_link}

## Body

> Hi {first_name}, Puneet. You have bought from us three times and then it went quiet, which usually means one of two things.
> Either life got busy, or something was not right the last time and you did not tell me.
> If it is the second one, tell me now. I would rather fix it than lose you.
> If it is the first, {last_product} is here when you want it: {reorder_link}

## The one CTA
A reply, or {reorder_link}. The reply matters more. A customer who tells you why they stopped is worth more than one who quietly reorders.

## When not to send
- Fewer than two lifetime orders. Those people get the first-to-second email instead, and this message would be factually wrong to them.
- Open complaint or unresolved refund
- Already received a win-back in the last 180 days. **Once per customer per six months, hard cap.**
- Asked to stop
- No WhatsApp marketing opt-in
- **They ordered in the last 60 days through a channel you cannot see.** Franchise walk-ins and corporate orders do not appear in online order history, so a Mumbai BKC regular can look lapsed while buying every fortnight. Check before sending to anyone in a franchise city.

## Compliance
WhatsApp category: **Marketing**. Marketing opt-in, template approval, and it counts against per-user limits. The hard cap above is not just courtesy, repeated marketing messages to a non-responder is how a WhatsApp Business number gets quality-rated down.

## Source
`my-work/voice-of-customer/2026-09-09-voc-report.md`. The gifter persona's "what would bring them back" line reads "the festival calendar, and there is no mechanism holding them between festivals". This is that mechanism. The "tell me now, I would rather fix it" register comes from the founder's real melt-complaint reply, where admitting the weakness kept the customer.

## SAFETY FLAGS
1. **"three times" is hardcoded in the body and it will be wrong for most recipients.** It has to become a token or a conditional before this ships. Left as written because it shows the intended register, but this line blocks the template.
2. **No discount, deliberately.** Same reason as the replenishment template. The brand never competes on price, so this win-back has to work on honesty and the calendar instead of on a percentage. That is harder and it is the correct constraint.
