# Session 6, Performance Marketer

**Time:** 100 minutes
**Primitive:** parallel dispatch, one parent subagent fanning out to several children
**Teammate hired:** 05, Performance Marketer
**You walk out with:** ads across two angles, a creative brief a designer could act on today, and at least one real rendered image

---

## Before you start

- [ ] `CLAUDE.md` filled, with the never-list and the claim wall in Section 7
- [ ] Market Analyst and Voice of Customer reports in `my-work/`
- [ ] The Content Lead index from Session 4, so your ads do not duplicate your organic plan
- [ ] `brand-brain/ads/ad-copy-bank.md` filled with ads that actually ran, if you have any

---

## What this teaches

Session 4 ran one subagent. This runs a parent that can spawn several children, each working a different angle at the same time.

**Why fan out at all.** Five ad angles written one after another in a single context bleed into each other. The third angle starts sounding like the first. Five children, each with a clean context and one angle, come back genuinely different.

The second idea in this session matters more than the parallelism: **change one thing at a time.** A variant that differs from your control on one axis teaches you something when it wins. One that differs on five teaches you nothing.

---

## Steps

### 1. Give it something to learn from

Before you run anything, make sure it has your ad history. Open `brand-brain/ads/ad-copy-bank.md` and paste in what actually ran, with any performance note you have. Even "no performance data" is useful, because it stops the agent assuming.

**If you run Meta ads,** connect the account so it can read live spend and creative rather than your memory of it. Click **+**, then **Connectors**, and look for the ads connector. If it is not there, paste a screenshot of your Ads Manager into the chat instead. Both work.

### 2. Run it

```
Use the performance-marketer agent to build this month's ads.
```

It sizes the run itself. Early stage or no ad history gets one angle. Everyone else gets two angles, five Meta ads and three Google headline sets each, with a creative brief per angle.

**To force specific angles:**

```
Use the performance-marketer agent with ANGLES=1,3
```

Where the five are: 1 hero product, 2 problem-solver, 3 anti-positioning, 4 social proof, 5 competitor gap.

**For everything, Sunday night:**

```
Use the performance-marketer agent with FULL_RUN=yes
```

That is five angles dispatched in parallel. **Watch the Tasks pane** when it runs: several rows appear at once, one per angle. Click between them to watch different children working. This is the moment parallel dispatch stops being an abstraction.

### 3. Read the winners pattern first

Before the ads, open `my-work/performance-marketer/<date>-winners-pattern.md`.

It extracts the shape of your past ads: dominant format, hook style, copy length, the CTA verb you keep reaching for, phrases that recur, and the one that usually matters most, **what is conspicuously absent from the set**.

Every new ad then either matches that pattern, which is the safe test, or breaks it on exactly one axis, which is a probe. Each ad says which it is in its own "why this works" line.

### 4. Read the index, then two ads

Open `my-work/performance-marketer/<date>-index.md`. It names the strongest ad in the strongest angle, the brief ready for a designer, the ad most likely to move whatever metric you are currently weakest on, and every safety flag.

Then read **two** ads: the control, and the one probe you find most interesting. Not all ten.

### 5. Work the flags

Ad copy flags are more expensive than content flags, because a rejected ad costs a review cycle and a bad claim costs more than that.

Look especially for:

- **Invented numbers.** Anything like "loved by 10,000 customers" must trace to a real source or become a placeholder.
- **Claims past your wall.** In food, anything about digestion or immunity. In cosmetics, anything clinical.
- **Named competitors.** Fine in your internal notes, not fine in ad copy.
- **Words on your never-list.** The agent checks, but check the flag list yourself.

### 6. Turn one angle into a creative brief

```
/creative-brief
```

It will ask which campaign, because a brief built on a guess wastes a designer's day. Name the angle you want to shoot.

You get one committed visual direction: the angle in a sentence, why now with the customer theme and its count, three things the visual must contain, tone from your always and never lists, what it must not show including your category's specific visual clichés, two craft references that are deliberately not competitors, and an image prompt.

**One direction, not five.** A designer handed five options has been given none.

### 7. Render it

Two routes, depending on whether you have a fal.ai key.

**With a key.** Put `FAL_KEY=your-key` in a file called `.env` at the repo root, then:

```
/fal-image-gen render the image prompt at the bottom of my latest creative brief, 4:5, save it to my-work/performance-marketer/creative/
```

Pick the mode by job: `t2i` for photography, `poster` when a headline is part of the artwork and must be legible, `i2i` to fan an approved shot across other products, `t2v` for a short video.

**Without a key.** It hands you the finished prompt to paste into whatever you already use, Midjourney, ChatGPT, Gemini, anything. **You lose nothing that matters.** The thinking is in the prompt. The key only changes where the pixels get made.

> **The one trap worth knowing.** If you are generating a variation from a reference image that has text on it, use strength 0.85 or above so the text drops cleanly and you add real copy afterwards. Between 0.50 and 0.80 the model tries to preserve letter shapes and produces something that looks right in a thumbnail and reads as nonsense up close. Never sit in that middle band.

### 8. Ship one ad

Take the control ad, the one that matches your winning pattern. Put it live with a small budget. The probe goes live next week, against it.

---

## Check it worked

- [ ] `my-work/performance-marketer/<date>-winners-pattern.md` exists and describes your real ads
- [ ] At least two angle folders, each with `meta.md`, `google.md` and `creative-brief.md`
- [ ] An index naming the strongest ad and every flag
- [ ] One creative brief with an image prompt and a negative prompt
- [ ] One image rendered, or one prompt saved ready to paste
- [ ] Every safety flag triaged

---

## If it breaks

**It says there is no ad history.**
It will say so once and carry on from your customer themes instead. Fill `brand-brain/ads/ad-copy-bank.md` before the next run.

**The ads are good but they all sound the same.**
Angles too close together. Force distance: `ANGLES=1,3` puts hero product against anti-positioning, which cannot converge.

**A rendered image has garbled text in it.**
Photography models cannot render legible copy at any strength. Use `poster` mode with the headline written verbatim into the prompt, or render clean and composite the text in a design tool.

**Parallel run stalled halfway.**
Check the Tasks pane for which child stopped. Re-run that one angle alone with `ANGLES=`, rather than restarting the whole fan-out.

**It dropped a word my customer actually used.**
It does this when a customer's own phrasing crosses your claim wall. It flags rather than silently removing. Read the flag, then overrule it if you have the substantiation.

---

## Take-home

Read [`references/module-6-performance-marketer/ad-angle-templates.md`](references/module-6-performance-marketer/ad-angle-templates.md) and [`visual-prompt-templates.md`](references/module-6-performance-marketer/visual-prompt-templates.md). Then re-run in Power scope with all five angles and pick your next month's tests from the set.

**Next:** [Session 7, Storefront and Marketplace](session-7-storefront-marketplace.md)
