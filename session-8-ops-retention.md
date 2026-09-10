# Session 8, Ops and Retention

**Time:** 90 minutes
**Primitive:** triggers, when X happens do Y
**Teammates hired:** 08 Ops Manager, 09 Retention Manager
**You walk out with:** SOPs with triggers precise enough to actually fire, a vendor template, WhatsApp and email flows, and two customer segments

---

## Before you start

- [ ] `CLAUDE.md` filled, including the anti-positioning in Section 3
- [ ] Voice of Customer report in `my-work/`, ideally the live-data one
- [ ] Store connected, if you want real returns and repeat data

---

## What this teaches

Both teammates in this session produce documents whose whole value is a **precisely defined trigger**.

"Stockout" is not a trigger. "Inventory below 20 units on a product that sold more than 50 last month" is a trigger, because somebody can tell you whether it has fired.

That is the discipline. An SOP with a vague trigger never runs. A retention message with a vague trigger sends to the wrong person at the wrong moment, which is worse than not sending.

The second idea is the section everybody skips: **when not to send.** A win-back landing on a customer with an open complaint does more damage than sending nothing at all.

---

## Steps

### 1. Write the operations down

```
/ops-manager
```

It picks the two SOPs your data says you need most, plus the one vendor template most likely to save you time this month, and **it tells you which two it picked and why before writing**, so you can redirect in one line.

The five it chooses from:

| SOP | Pays off when |
|---|---|
| Stockout response | A top product runs out and everyone scrambles |
| Returns spike | Returns on one product jump in a week |
| Freelancer onboarding | You brief every new hire from scratch |
| New product launch | The eighteen things between deciding and going live |
| Press or influencer inquiry | Separating real opportunities from time-wasters |

### 2. Check the triggers can actually fire

Open each SOP and read the `Trigger:` line at the top. Ask yourself one question: **could someone who is not me tell whether this has fired today?**

If no, rewrite it until yes. That is a two minute edit and it is the difference between a document and a system.

### 3. Read the escalation point

Every SOP names the moment you stop following it and call the founder. In food and cosmetics, anything involving an allergen, foreign matter or a customer reporting illness escalates immediately, before the rest of the playbook runs.

**Check that line matches your category.** It is written from your `CLAUDE.md` compliance section, so if it looks thin, your compliance section is thin.

### 4. Build the retention flows

```
/retention-manager
```

It writes the five moments where customers quietly slip away:

| Moment | Fires | Channel |
|---|---|---|
| Order confirmation | On payment | Email for the record, WhatsApp for the warmth |
| Delivery check-in | 3 days after delivery | WhatsApp |
| Replenishment | Consumption window minus 7 days | WhatsApp |
| Win-back | 60 days quiet, from a repeat buyer | Both |
| First to second purchase | 21 days after a first order | Email |

Plus two segments defined as **runnable filters**, not descriptions. "Two or more orders in the last 180 days, most recent within 60 days" is a segment. "Loyal customers" is not.

### 5. Read the WhatsApp templates out loud

Genuinely, out loud.

WhatsApp arrives in the same thread as messages from someone's family. It either sounds like you or it should not send. Email can be a brand. WhatsApp cannot.

If a line makes you wince, change it in the file. That file is what gets loaded into your WhatsApp Business platform.

### 6. Check the compliance section on every template

Stricter here than anywhere else in the bootcamp, because the downside is an account ban rather than an awkward sentence.

- **Marketing templates need opt-in and platform approval.** Utility templates, like an order confirmation with no offer in it, are treated differently. Each template says which it is.
- **Every marketing message needs a way to stop receiving them.**
- **Email needs an unsubscribe link.** Not optional under India's DPDP Act.
- **No invented offers.** If a discount appears that you did not authorise, it will eventually become a discount you have to honour.

### 7. Notice what your anti-positioning rules out

If your `CLAUDE.md` says you never compete on price, then the standard win-back discount and the standard subscribe-and-save are both unavailable to you.

That is a harder brief and the correct one. Read how the win-back works without an offer. It is usually more honest than the discount version, and it is the clearest example this weekend of `CLAUDE.md` shaping output three sessions downstream.

### 8. Ship one moment

Load **one** template into your WhatsApp Business platform and set its trigger. Watch it for two weeks.

All five at once and you will never know which one worked.

---

## Check it worked

- [ ] `my-work/ops-manager/sops/` has two SOPs, each with a trigger someone else could evaluate
- [ ] `my-work/ops-manager/vendor-kit/` has a vendor template with placeholders, not invented names
- [ ] `my-work/retention-manager/whatsapp/` and `/email/` have templates
- [ ] Every template has a filled "when not to send" section
- [ ] `my-work/retention-manager/segments/` has two segments written as filters
- [ ] One retention moment is live, with the date you switched it on

---

## If it breaks

**The SOPs are for problems I do not have.**
Tell it what is actually happening: "I am hiring a freelancer next month and fielding press. Write those two instead."

**A segment has no size in it.**
It will not estimate customer counts it cannot see. Connect the store, or paste the numbers and ask it to fill them.

**The replenishment timing looks wrong.**
It derives that from your data, and if it only has one data point it says so. Check the flag. Run it against one cohort before rolling it out to everybody.

**A template feels pushy.**
Say which line and why. Most of these skills carry a rule against upselling, so a pushy line usually means it inherited something from your own past copy.

---

## What good looks like

[`examples/the-paan-legacy/my-work/ops-manager/`](examples/the-paan-legacy/my-work/ops-manager/) and [`retention-manager/`](examples/the-paan-legacy/my-work/retention-manager/).

Read [`references/module-8-ops-retention/hooks-and-triggers.md`](references/module-8-ops-retention/hooks-and-triggers.md) for how to wire a trigger to something that actually watches for it.

---

## Take-home

Put the SOPs where your team already looks. A folder nobody opens is the same as not writing them. Keep the WhatsApp templates one click from the inbox, since that is where most of them get used.

**Next:** [Session 9, Growth Analyst](session-9-growth-analyst.md)
