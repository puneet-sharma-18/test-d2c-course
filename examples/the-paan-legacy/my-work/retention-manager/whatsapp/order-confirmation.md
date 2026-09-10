# WhatsApp, Order confirmation
Fires: immediately on successful payment. Within 2 minutes.
Segment: everyone. This is the only template with no segment condition.
Tone: warm, first person, signed. Not a receipt. The email is the receipt.
Personalisation tokens: {first_name}, {product}, {order_number}, {dispatch_date}

## Body

> Hi {first_name}, this is Puneet. Order {order_number} is in.
> Your {product} gets rolled on {dispatch_date} and goes out the same morning. It is not sitting in a warehouse waiting for you.
> Two things when it arrives. Put it in the fridge. Eat it whole, do not spit.
> Reply here if anything is wrong. I read this.

## The one CTA
No link. This message deliberately has no call to action. The customer has just paid. Asking them to do anything else is the upsell the brand does not do.

## When not to send
- Order failed, cancelled or payment pending
- A duplicate of an order confirmed in the last 10 minutes
- Customer has no WhatsApp opt-in. Send the email only.

## Compliance
WhatsApp category: **Utility**. Post-purchase transactional, so it does not need marketing opt-in, but it still needs template approval before first send. Confirm the category with your BSP, because a Utility template that reads as promotional gets reclassified and then it needs marketing opt-in retroactively. This one has no offer and no link, which is what keeps it Utility.

## Source
`CLAUDE.md` Section 7 voice rules, the packaging insert voice, and the eating instruction from the live Meetha Paan product page. The "I read this" line is taken from the brand's own thank-you card, which reads "If a paan is broken, the rose is missing, or the saffron is shy, reply on WhatsApp. I read it."
