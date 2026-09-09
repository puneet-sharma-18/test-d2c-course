# Vendor email, Purchase order confirmation
Use when: placing or confirming a production order, especially the festival build. Send this for every order above {value-threshold}, and for every order at all between now and Diwali.
Tone: professional and direct. Often read in the recipient's second language, so keep sentences short. One fact per line.

## Subject lines
1. PO {po-number} confirmation, delivery {delivery-date}
2. Order confirmation, {quantity} {product}, delivery {delivery-date}
3. Please confirm in writing, PO {po-number}

## Body

> Dear {vendor-name},
>
> Please confirm this order in writing by replying to this email.
>
> PO number: {po-number}
> Product: {product-and-grade}
> Quantity: {quantity} {unit}
> Unit price: ₹{unit-price}
> Total value: ₹{total-value}
> Delivery date: {delivery-date}
> Delivery address: {address}
>
> Quality specification:
> {spec-line-1}
> {spec-line-2}
>
> Three things I need confirmed, not assumed:
> 1. The unit price above is fixed for this order. If your input cost has moved since our last order, tell me now, before dispatch, not on the invoice.
> 2. The delivery date above is a committed date. If you cannot meet it, reply today with the date you can meet.
> 3. Each delivery must carry a batch code and a packing date. We trace quality complaints back to the batch.
>
> If any of the three is a problem, call me on {phone} rather than replying.
>
> Regards,
> Puneet
> The Paan Legacy
> FSSAI {license-number}

## Attach
- The signed purchase order
- The written quality specification for this input
- The previous batch report, where a defect was raised on the last order

## What not to write
- Do not leave price open with "as per market rate". That is where saffron and other moving inputs quietly reprice at invoice.
- Do not accept a verbal delivery date and write "confirmed" in your own notes. It is confirmed when they write it.
- Do not raise a past quality problem in the same email as a new order without attaching the batch evidence. It reads as a negotiating move rather than a quality issue and it hardens the vendor.
- Do not mention that you are short on stock. It weakens the price conversation.

## If no reply in 2 days
Call. If there is still no written confirmation 3 days after sending, treat the date as unavailable, and trigger `sops/stockout-response.md` on the affected SKU rather than waiting. For inputs with a single vendor, granola being the known one, start the second vendor conversation the same day.
