# Session 5, Day 1 Integration

**Time:** 45 minutes
**Primitive:** synthesis across teammates, a first taste of the Captain pattern
**You walk out with:** one cross-cutting read of everything Day 1 produced, and one thing chosen to ship Monday

---

## Before you start

- [ ] `CLAUDE.md` filled
- [ ] Market Analyst report in `my-work/`
- [ ] Voice of Customer report in `my-work/`
- [ ] Content Lead calendar, pieces and index in `my-work/`

If any of those is missing, this session has nothing to synthesise. Go back and fill the gap first.

---

## What this teaches

You now have four teammates and a folder of output. The risk at this exact moment is that you have **files instead of decisions**.

Every teammate so far could only see its own slice. The Market Analyst does not know what your customers said. The Voice of Customer does not know what your competitors are doing. Nobody has read all four.

Reading across them is a different job, and it is the one that produces the finding worth acting on.

---

## Steps

### 1. Take stock, out loud

```
List every file in my-work/, grouped by teammate, with the date each was produced. Then tell me in three lines what I have and what is missing.
```

This takes ten seconds and reframes the day. You built four teammates and a body of work.

### 2. Run the day one synthesis

Open [`references/module-5-integration/captain-day-1.prompt.md`](references/module-5-integration/captain-day-1.prompt.md) and paste the prompt it contains.

If you would rather type it fresh, this is the shape:

```
Read CLAUDE.md, the latest report in my-work/market-analyst/, the latest in my-work/voice-of-customer/, and the index in my-work/content-lead/. Do not read individual content pieces.

Then answer four things:
1. The single strongest signal across all three, and which files support it.
2. Anywhere two teammates disagree with each other, or with CLAUDE.md.
3. The one thing I should ship on Monday, and why that one.
4. The cheapest piece of data I could get this week that would sharpen every teammate at once.

One recommendation, not five. If one teammate could have said it alone, it does not count.
```

### 3. Judge the answer hard

A good cross-cutting finding sounds like this:

> Your customer research shows a theme rising in eight of twenty-seven messages, your competitor report shows nobody in the category serving it, and your content calendar has one piece against it in week four. Move that piece to week one and build the product page for it this week.

Three teammates pointing the same way at something none of them could see alone.

**A bad one sounds like:** "your customers care about quality and your competitors are strong on distribution." That is a summary. Push back and ask for the specific counts and the specific files.

### 4. Chase the disagreements

Question 2 is where the value hides. Common ones:

- Your `CLAUDE.md` describes a customer your reviews do not support
- Your product data ranks a SKU highly that your customers rate poorly
- A competitor you consider a rival never gets mentioned by a single customer

**Do not resolve these by picking a side.** Write the disagreement into `CLAUDE.md` under known gaps, so every teammate on Day 2 works with the uncertainty visible rather than inheriting a guess.

### 5. Pick Monday's ship

One thing. Name it, name the day, name what has to be true for it to go out.

Write it at the top of a file:

```
Create my-work/captain/<today>-day-1-summary.md with: the strongest signal and its sources, the disagreements found, the one thing shipping Monday with its date, and the one data gap to close this week.
```

### 6. Close the cheapest data gap

Question 4 usually returns something dull and high value: export your full review set, get a real cohort pull, find your FSSAI number, fill the pack weights.

**Do that one thing tonight.** Day 2 sessions all read the same inputs, so one gap closed now improves five sessions tomorrow.

---

## Check it worked

- [ ] `my-work/captain/<date>-day-1-summary.md` exists
- [ ] It names one cross-cutting finding with the files that support it
- [ ] It lists at least one disagreement between teammates or with `CLAUDE.md`
- [ ] One thing is named for Monday, with a date
- [ ] One data gap is named, and you know how to close it

---

## If it breaks

**The synthesis is bland.**
It probably read the content pieces and drowned. Tell it explicitly: indexes and reports only, never individual pieces.

**It gave me five recommendations.**
Ask for one. "If everything is a priority, nothing is" is the standard. Make it choose and justify.

**It found no disagreements.**
Sometimes true, usually not. Push: "compare the primary customer in CLAUDE.md Section 5 against the customers actually present in the VoC report, and tell me every way they differ."

---

## Day 1 is done

You can now answer the four questions that make Day 2 easy:

- **What is in `CLAUDE.md`?** Your brand, in a file every teammate reads first.
- **What is a skill?** A written job description Claude loads when it fits.
- **What is a connector?** The plug to your live systems.
- **What is a subagent?** A teammate with its own context for big jobs.

Tomorrow is the same four ideas applied to growth and operations.

**Next:** [Session 6, Performance Marketer](session-6-performance-marketer.md)
