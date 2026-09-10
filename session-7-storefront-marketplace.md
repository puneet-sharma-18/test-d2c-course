# Session 7, Storefront and Marketplace

**Time:** 90 minutes
**Primitive:** live data iteration, read the numbers, find the gap, rewrite, save as a draft
**Teammates hired:** 06 Storefront Specialist, 07 Marketplace Editor
**You walk out with:** two product pages rewritten with a before and after, CRO observations tied to evidence, and marketplace listings

---

## Before you start

- [ ] Store connected from Session 3, or conversion data you can paste
- [ ] Voice of Customer report in `my-work/`
- [ ] Market Analyst report in `my-work/`
- [ ] `brand-brain/nominated-skus.md` filled, if you want to choose the pages yourself

---

## What this teaches

Every session so far produced something new. This one **changes something that already exists**, which is a different discipline.

The loop is: read how a page is actually performing, find the gap between what it says and what customers care about, rewrite to close that gap, and save it as a draft for a human to approve.

**The rule that makes it work: never publish, always draft.** Even with write access, these teammates hand you a draft. You decide.

The second rule is about measurement. **Ship one page, wait a week, then do the next.** Changing four pages at once tells you nothing about which change worked, and you will have burned the only clean read you were going to get.

---

## Steps

### 1. Rewrite two product pages

```
/pdp-writer
```

It picks by evidence rather than by taste: the two lowest-converting pages among your top five by orders. High traffic and low conversion is where a rewrite pays.

**It says which pages it picked and why before it writes anything.** If you would rather it worked on the SKUs in `brand-brain/nominated-skus.md`, say so now.

For each page it produces three things:

| File | What it is |
|---|---|
| `<date>-<slug>-before.md` | What is live now, plus a five line gap analysis |
| `<date>-<slug>-after.md` | The rewrite, with sources |
| `<date>-cro-observations.md` | Five observations across page, cart and checkout |

### 2. Read the gap analysis before the rewrite

This is the diagnostic and it is more useful than the copy.

```
The page leads with: ...
Customers actually care about: ... (with a count)
Competitors emphasise, and we do not: ...
Unanswered here, but asked constantly in support: ...
Biggest conversion blocker, best guess: ...
```

If that reads true, the rewrite will be good. If it reads wrong, fix the diagnosis, not the copy.

### 3. Read the CRO observations

Each one carries where, the issue, the **evidence**, the fix, an impact rating and an effort rating.

**An observation with no evidence is an opinion.** The skill is told to cut those. If one slipped through with vague reasoning, delete it yourself.

Sort them by impact over effort and do the top one this week.

### 4. Rewrite the marketplace listings

```
/marketplace-editor
```

This one holds a specific idea in its head the whole time: **the marketplace shopper is not the same person as your website shopper.**

| | Your site | Amazon or Flipkart |
|---|---|---|
| How they arrived | Your content, your brand | A generic search, comparing |
| They read first | Hero image and line | Title, price, star rating |
| They trust | Your brand | The reviews on this listing |
| They fear | "Is this worth it?" | "Is this fake, old stock, wrong size?" |
| Time on page | About 90 seconds | About 25 seconds |

So the copy gets denser and more spec-forward, the story moves to the third module, and the title carries the terms people filter on.

### 5. Handle the compliance fields properly

Marketplace listings are where compliance stops being abstract. Every listing needs:

- **Net weight.** Not optional in a food or cosmetics category.
- **Your real licence number.** FSSAI, CDSCO or Ayush as applicable.
- **Allergens, per SKU.**
- **A marketed-by entity.**

The skill leaves these as placeholders rather than inventing them, and flags each one as blocking. **A blank field is recoverable. A wrong allergen declaration is not.** Get the real values before you upload anything.

### 6. Push one page as a draft

If your store is connected:

```
Push the rewritten page for <SKU> to my store as an unpublished draft. Do not publish it.
```

If it is not connected, copy the after file into your store admin by hand and save it as a draft there.

**Then stop.** One page. Measure for seven days. The second page goes live next week.

---

## Check it worked

- [ ] `my-work/storefront-specialist/` has a before, a gap and an after for two pages
- [ ] `<date>-cro-observations.md` has five observations, each with real evidence
- [ ] `my-work/marketplace-editor/` has listings for at least one product on both platforms
- [ ] Every compliance placeholder is either filled with a real value or marked as blocking
- [ ] Exactly one page is live or in draft, and you wrote down the date you shipped it

---

## If it breaks

**It picked pages I do not care about.**
It picks on conversion data. Override it: "rewrite the pages for the SKUs in brand-brain/nominated-skus.md instead, and tell me what that costs me versus your picks."

**It could not read my live page.**
It will record the before state as not captured and say so rather than inventing your current copy. Paste the live page into the chat and it becomes real.

**The listing is for a platform I am not on.**
It will say so in the index and write the listing as a launch listing rather than a rewrite. Worth reading anyway: it usually tells you whether your product actually suits that channel, which is a bigger question than the copy.

**It refused to tick a gluten-free box.**
Because nothing in your `CLAUDE.md` states the gluten status for that SKU. That refusal is the system working. Get the real answer and add it to your profile.

---

## What good looks like

[`examples/the-paan-legacy/my-work/storefront-specialist/`](examples/the-paan-legacy/my-work/storefront-specialist/) has a full before, gap and after set, plus CRO observations. [`examples/little-lab/my-work/marketplace-editor/`](examples/little-lab/my-work/marketplace-editor/) is the better read for a marketplace-heavy brand, since Little Lab sells mostly on Amazon and Flipkart.

---

## Take-home

Read [`references/module-7-storefront-marketplace/cro-iteration-loop.md`](references/module-7-storefront-marketplace/cro-iteration-loop.md). Then set a calendar reminder for seven days out to read the numbers on the page you shipped. That reminder is the actual skill this session is teaching.

**Next:** [Session 8, Ops and Retention](session-8-ops-retention.md)
