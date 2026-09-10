# Email, Order confirmation
Fires: immediately on successful payment, alongside the WhatsApp message.
Segment: everyone.
Tone: this one is the record. Warmer than a receipt, shorter than a letter.
Personalisation tokens: {first_name}, {product}, {order_number}, {dispatch_date}, {order_total}, {delivery_address}

## Subject lines
1. Order {order_number}, rolling on {dispatch_date}
2. {first_name}, your paan gets rolled on {dispatch_date}
3. Order {order_number} confirmed

## Body

> Hi {first_name},
>
> Order {order_number} is confirmed. Here is what happens next.
>
> Your {product} gets hand-rolled on the morning of {dispatch_date} and goes out the same day. We do not make to stock, so nothing in that box was sitting in a warehouse.
>
> **When it arrives**
> Refrigerate it as soon as it reaches you. Best within 14 days of dispatch.
> Eat each one whole, in one piece. Do not bite it and put it down. Do not spit. The leaf is meant to be swallowed.
> If it is your first time, eat half and drink water.
>
> **If you live in Delhi, Hyderabad or Lucknow between May and August**, reply and ask for summer shipping. We send it in an insulated box at no extra cost. You should not have to know to ask for this, and we are working on that.
>
> If a paan is broken, the rose is missing or the saffron is shy, reply to this email or message us on WhatsApp. I read both.
>
> Puneet
> The Paan Legacy
> FSSAI {fssai_license_number}
>
> Order total {order_total}. Shipping to {delivery_address}.
> {unsubscribe_link}

## The one CTA
None. This is a confirmation. The only actions offered are storage instructions and a reply address.

## When not to send
- Payment pending or failed
- Duplicate send on the same order number

## Compliance
Transactional email, so it is exempt from marketing consent under the DPDP Act, but **the unsubscribe link is present anyway** because the same template will get reused for something promotional eventually and that is when it bites. FSSAI licence number appears in the footer, which is standard for food commerce in India.

## Source
The storage and eating instructions are verbatim in structure from the live Meetha Paan and Almond Delight product pages. The summer shipping line is from the same pages, where the offer currently sits buried in an order-notes field, flagged as a cart problem in `my-work/storefront-specialist/2026-09-10-cro-observations.md`.

## SAFETY FLAGS
1. **`{fssai_license_number}` is a placeholder.** The number does not appear anywhere in this repo and it has now blocked five separate deliverables. It is required on Indian food commerce email.
2. **The summer shipping paragraph should be conditional on month and pin code**, not sent year round. Sending it in December makes the brand look like it is not paying attention.
