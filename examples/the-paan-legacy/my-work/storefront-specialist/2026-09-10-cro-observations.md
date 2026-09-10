# CRO observations, The Paan Legacy
Date: 2026-09-10
Run: default, 5 observations

### The question that gates the sale is answered below the fold
- Where: every paan product page, and the cart
- Issue: customers ask whether this is spit-out paan or eat-and-swallow **before** they pay, and the page makes them hunt for it.
- Evidence: Voice of Customer theme 1, 5 of 27 messages. One customer asked it on WhatsApp before ordering. Another wrote "Bought because the page said spit-free. Confirmed." A third: "I cannot remember the last time I ate a paan I did not have to spit out. This is the first."
- Fix: put "Eat, do not spit. No tobacco. No supari." as a fixed line directly under the price on every paan page, and repeat it in the cart. It is already the brand refrain, so this costs nothing to write.
- Impact: high
- Effort: day

### The site title tag breaks two voice rules and buries the term people filter on
- Where: home page and site-wide title template
- Issue: the indexed title reads "Gourmet Paans, Premium Mukhwas & Traditional Sweets". Two words on the never-list, plus "Traditional Sweets", which argues the brand is a sweet shop when the entire wedge is that it is not.
- Evidence: `2026-09-09-intel-report.md`, "Where this contradicts your file", item 5. Same failure already found in the Google Search headline, so this is the second instance in the highest-traffic copy.
- Fix: rewrite to lead with the filter term and the differentiator, for example "Tobacco-free paan and hand-roasted mukhwas, delivered". Drop the sweets claim entirely.
- Impact: medium
- Effort: day

### Four customers told you when they would come back and checkout captured none of it
- Where: checkout
- Issue: repurchase intent arrives unprompted with a date attached, and there is no mechanism to hold it. The workaround is a manual reminder list currently running for one person.
- Evidence: Voice of Customer theme 8, 4 of 27 messages carry dated intent, "will try again in winter", "will reorder in October", "will buy again for special occasions". A three-time buyer wrote "Need a subscribe-and-save. Reordering manually every six weeks is annoying." Repeat rate is 30%, the strongest number in the business.
- Fix: one checkbox at checkout, "remind me in six weeks", no payment stored and no subscription. That is exactly what was offered by hand on WhatsApp and accepted within two minutes.
- Impact: high
- Effort: week

### Gifting is the cheapest acquisition channel and the checkout does not know it exists
- Where: cart and checkout
- Issue: no recipient address, no delivery date, no gift message. Every gift order is currently a normal order with instructions typed into a free-text box, if at all.
- Evidence: Voice of Customer theme 4, 6 of 27 messages involve a gift and 4 document a recipient who then went looking for the brand. The corporate lead in the same report found the brand through a colleague's wedding favours. `2026-09-09-intel-report.md` names occasion-led gifting as the content gap and shows 13 of 25 ads in the corporate search running live against it.
- Fix: a gift toggle on the product page that captures recipient address, a required delivery date and a short message. The delivery date matters most, because a late gift is a lost referral.
- Impact: high
- Effort: week

### The free insulated box is hidden inside a free-text order note
- Where: cart
- Issue: the summer shipping upgrade is free and already exists, and the customer only gets it if they know to type "summer shipping" into the order notes. Customers who do not know keep receiving melted product.
- Evidence: the live Meetha Paan and Almond Delight pages both say to mention it in the order notes. Voice of Customer theme 5 records melt reaching a customer anyway. `CLAUDE.md` traces CAC drift from ₹447 to ₹475 to hot pin codes, and prices the melt exposure at 3 to 5 margin points on two SKUs.
- Fix: detect the pin code at cart and apply the insulated box automatically for the affected cities and months, or failing that a visible checked box rather than a free-text field.
- Impact: medium, rising to high between May and August
- Effort: week
