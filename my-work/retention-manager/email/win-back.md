# Email, Win-back
Fires: **62 days after the last delivery**, on a customer with two or more lifetime orders, and only if the WhatsApp win-back sent 48 hours earlier got no reply.
Segment: `repeat-buyers` gone quiet.
Tone: no guilt. No "we miss you". No offer.
Personalisation tokens: {first_name}, {last_product}, {order_count}, {reorder_link}

## Subject lines
1. {first_name}, did we drop something?
2. Two months quiet
3. A question rather than an offer

## Body

> Hi {first_name},
>
> You ordered from us {order_count} times and then it stopped, about two months ago.
>
> I am not going to send you a discount to come back. We do not compete on price and a code would be the wrong way to ask.
>
> So instead, a question. Did something go wrong? A box that arrived soft, a delivery that took too long, a paan that was not what you expected. If any of that happened and you did not tell me, tell me now. I would rather fix it than lose you quietly.
>
> If nothing went wrong and life just moved on, that is fine too. {last_product} is here when you want it: {reorder_link}
>
> Either way, thank you for the {order_count} orders. That is more than most.
>
> Puneet
> The Paan Legacy
>
> {unsubscribe_link}

## The one CTA
A reply. {reorder_link} is secondary and deliberately placed after the question.

## When not to send
- Fewer than two lifetime orders
- Open complaint or refund
- A win-back sent in the last 180 days. **Hard cap, once per six months.**
- No reply needed if they replied to the WhatsApp version. That reply is the win, stop the flow.
- Franchise city customers who may be buying offline where you cannot see it
- No marketing consent

## Compliance
Marketing email. Consent required, unsubscribe mandatory. **No offer, so nothing to substantiate.** Explicitly refusing to discount is both on-brand and the compliance-simplest option available.

## Source
`CLAUDE.md` Section 3 anti-positioning, "never compete on price", which rules out the standard win-back discount and forces this message to work on honesty instead. The condition-not-taste finding in `my-work/voice-of-customer/2026-09-09-voc-report.md` theme 5 is why the question asks about the box rather than about the paan.

## SAFETY FLAGS
1. **This flow has two emails maximum and then it stops.** As written there is one. If anyone adds a third, the exit condition has to come with it. A win-back with no stopping rule eventually mails someone who has ignored eleven messages, and that is how sender reputation dies.
