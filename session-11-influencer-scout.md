# Session 11, Influencer Scout (add-on)

**Time:** 60 minutes
**Primitive:** none new, this is a skill applied to a job you would otherwise pay an agency for
**Teammate hired:** Influencer Scout
**You walk out with:** a shortlist of creators with red-flag checks, first-touch outreach for each, and a counter-offer script

---

## Before you start

- [ ] `CLAUDE.md` filled, especially Section 5, your customer, and Section 3, your anti-positioning
- [ ] Voice of Customer report in `my-work/`, so the outreach can speak to real themes
- [ ] A creator pool to filter, see step 1

This is an add-on. It sits outside the core ten and you run it when the brand needs the muscle, not because it is next in the list.

---

## What this teaches

Creator selection is where most D2C money gets wasted, and it gets wasted in a specific way: **the brand picks on follower count, the agency picks on availability, and nobody checks whether the creator's audience is the brand's customer.**

This skill does the boring part properly. It filters a pool against your actual category and audience, runs red-flag checks, and drafts outreach that sounds like you rather than like a template.

It will not tell you a creator is good. It will tell you which ones are plausible and what to check before you pay.

---

## Steps

### 1. Get a creator pool

**If you use Modash, Upfluence or similar,** export a search as JSON or CSV and drop it in `brand-brain/`.

**If you do not,** use the sample pool shipped with the bootcamp:

```
Use references/module-11-influencer-scout/sample-creator-pool.json as my creator pool.
```

It is realistic in shape, so you learn the filter logic and the negotiation, and you swap in real data later. Read [`references/module-11-influencer-scout/modash-data-shape.md`](references/module-11-influencer-scout/modash-data-shape.md) to see what fields matter, so your own export carries them.

### 2. Run it

```
/influencer-scout
```

It reads your brand profile, filters the pool against your category and audience, and produces a shortlist with a reason for each name.

Default is five creators. For more:

```
/influencer-scout give me ten creators and a four week ladder
```

### 3. Read the red flags before the names

The skill checks for the things that cost money: engagement that does not match follower count, audience geography that does not match where you ship, comment patterns that suggest bought engagement, and category mismatch dressed up as adjacency.

**Read [`references/module-11-influencer-scout/red-flag-cheatsheet.md`](references/module-11-influencer-scout/red-flag-cheatsheet.md) once**, then you can spot most of these yourself in future without running anything.

### 4. Sanity-check the rates

Open [`references/module-11-influencer-scout/rate-card-benchmarks-india.md`](references/module-11-influencer-scout/rate-card-benchmarks-india.md).

Compare what the shortlist suggests against the benchmark band for that tier. If a quote comes back at three times the band, that is a negotiation, not a rejection, and the next step is where you handle it.

### 5. Read the outreach in your own voice

Each shortlisted creator gets a first-touch message. It should read like you wrote it, because it was written from your voice rules.

**Check one thing specifically:** does it say what you want clearly, or does it open with flattery and bury the ask? The second one gets ignored, and it is the default failure mode of brand outreach.

### 6. Learn the counter-offer script

Open [`references/module-11-influencer-scout/negotiation-playbook.md`](references/module-11-influencer-scout/negotiation-playbook.md).

The counter-offer script matters more than the outreach, because the outreach gets you a reply and the counter-offer decides what you pay. Read it before you send anything, so the first number you hear does not anchor you.

### 7. Send three

Not ten. Three, so you can tell which framing got a reply.

---

## Check it worked

- [ ] `my-work/influencer-scout/<date>-shortlist.md` exists with reasons per creator
- [ ] Every creator carries a red-flag check, not just a follower count
- [ ] Outreach reads in your voice and states the ask in the first three lines
- [ ] You read the negotiation playbook before sending
- [ ] Three messages sent

---

## If it breaks

**Every creator it picked is too big for my budget.**
Give it the constraint: "shortlist only creators under 50k followers, and tell me what I lose by capping there."

**The outreach sounds like a brand.**
Your `brand-brain/voice-dna/` is thin, or the skill is not reading it. Paste two things you actually wrote into the chat and ask it to redraft from those.

**The pool has no engagement data.**
Then it cannot run red-flag checks, and it will say so rather than guessing. Export again with engagement fields included, using the data-shape reference.

---

## What good looks like

[`examples/the-paan-legacy/my-work/influencer-scout/`](examples/the-paan-legacy/my-work/influencer-scout/).

---

## Take-home

Re-run monthly with a fresh pool. Keep a note of which framing got replies. After three rounds you will know your own outreach better than any playbook can tell you.

**Back to:** [Student Handbook](student-handbook.md)
