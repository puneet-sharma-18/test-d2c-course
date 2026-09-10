# Session 10, Capstone

**Time:** 75 minutes
**Primitive:** the Captain pattern, one subagent reading across every other teammate
**Teammate hired:** the Captain
**You walk out with:** a 90 day operating roadmap, a standing schedule, and one recommendation no single teammate could have made

---

## Before you start

- [ ] Every session from 1 to 9 has produced at least one file in `my-work/`
- [ ] `CLAUDE.md` is current, ideally refreshed since Session 2

If three or more teammates never ran, the Captain will say so and its synthesis will be thin. That is honest behaviour, not a bug. Better to run the missing teammates first.

---

## What this teaches

You have ten teammates and a folder with dozens of files in it. Nobody has read all of it, and nobody could: reading every ad, SOP and page would fill any context before a single conclusion got drawn.

The Captain solves that with one rule.

**Indexes only, never raw outputs.** Every teammate writes a short index precisely so the Captain never has to open their work. Ten indexes is a manageable read. Two hundred pieces is not.

That rule is what makes an orchestrator possible at all, and it is why every session this weekend insisted on writing an index you probably skimmed.

---

## Steps

### 1. Check the chain is alive

Before synthesis, take stock:

```
For each folder in my-work/, tell me the most recent file and how many days old it is. Flag anything older than 14 days.
```

A stale chain is the most common reason a Captain run is worthless, and it is invisible unless you name it. If most of your work is from this weekend, you are fine.

### 2. Run the Captain

```
Use the captain agent to produce my 90 day roadmap.
```

It reads `CLAUDE.md`, the two reports, and one index per teammate. Watch the Tasks pane: you should see it opening indexes, not pieces. If it starts reading individual ads, stop it and remind it of the rule.

It produces two files:

- `my-work/captain/<date>-90-day-roadmap.md`, the thing you consult
- `my-work/captain/<date>-summary.md`, the thing you actually read

### 3. Read the summary first

Two lines on the state of the chain, the cross-cutting recommendation, a pointer to the roadmap, and one to three things needing your attention right now, ranked.

### 4. Judge the cross-cutting recommendation

**This is the entire reason the Captain exists**, so hold it to the standard.

A good one looks like: your customer research shows a theme rising, your competitor work shows nobody serving it, so paid should ship that angle, content should bias toward it, and the product page gets rewritten this week. **Three or more teammates moving together on a signal none of them could see alone.**

**If one teammate could have said it by reading only their own output, it is not a Captain recommendation.** Push back and ask for one that cites at least three.

### 5. Work the roadmap

Week 1 gets three to five items. Each names the action, which teammate runs it, the measurable outcome, and **what it costs you if it does not happen**. That last column is what makes a roadmap something you act on rather than something you file.

Months 2 and 3 get three priorities each and no more. If your month 2 has nine items, it has none.

### 6. Settle the standing schedule

The roadmap recommends a schedule rather than setting it up. Read it, decide what you actually want, then wire the ones you will keep.

A realistic starting set for a founder with a day job:

| When | Who | What |
|---|---|---|
| Monday 09:00 | Growth Analyst | The weekly brief, already set up in Session 9 |
| Monday 09:30 | Market Analyst | What moved in the category last week |
| Monthly | Content Lead | Next 30 day calendar |

**Three is plenty.** Six recurring jobs that all ping you is how people end up muting the whole system.

Set each one up in the **Routines** sidebar the same way you did in Session 9, with the same discipline: short ping, detail in the file, test one before scheduling the rest.

To have the Captain wire them for you instead of listing them:

```
Use the captain agent with WIRE_SCHEDULE=yes and DELIVERY=email to set up the recurring runs.
```

It needs both flags. Passing the first without a delivery target gets you a checklist rather than a schedule, deliberately, because a recurring job with nowhere to deliver runs silently for weeks and nobody notices.

### 7. Read what it could not synthesise

The last section of the roadmap names the teammates whose output is stale and the questions it could not answer because the data is not there.

**That list is your next month's homework**, and it is usually more actionable than the roadmap itself.

---

## Check it worked

- [ ] `my-work/captain/<date>-90-day-roadmap.md` exists
- [ ] `my-work/captain/<date>-summary.md` exists and you read it first
- [ ] The cross-cutting recommendation cites at least three teammates
- [ ] Week 1 has three to five items, each with an owner and a cost of inaction
- [ ] Your standing schedule is set up, tested, and no more than three jobs
- [ ] You know which data gap to close first

---

## If it breaks

**The recommendation is something one teammate already told me.**
Reject it. "Give me one that requires reading at least three teammates, and name them."

**It says my chain is stale.**
Believe it. Re-run the two or three teammates it named, then run the Captain again. A roadmap built on month-old inputs reads exactly as confident as a good one, which is what makes it dangerous.

**It ran out of room partway through.**
It read raw outputs instead of indexes. Restart it and say explicitly: "read only the index file from each teammate folder, never the pieces, ads, SOPs or pages."

**It wired nothing after I asked it to.**
`WIRE_SCHEDULE=yes` needs `DELIVERY=` alongside it. Check both were in your message.

---

## What good looks like

[`examples/the-paan-legacy/my-work/captain/`](examples/the-paan-legacy/my-work/captain/) and [`examples/little-lab/my-work/captain/`](examples/little-lab/my-work/captain/) each have a day one summary, a 90 day roadmap and a summary.

Read [`references/module-10-capstone/standing-schedule.md`](references/module-10-capstone/standing-schedule.md) before you wire anything.

---

## You are done

Ten teammates, all operating on your brand. A weekly brief that arrives without being asked. A 90 day plan with owners.

**What to do in the next seven days:**

1. Do the Week 1 items on the roadmap.
2. Close the one data gap the Captain named.
3. Read the Monday brief when it lands, and do its one action.

**Then come back.** Re-run any teammate by opening its session file. They compound. The Brand Brain gets richer, the Market Analyst builds history, the Growth Analyst finally gets trends once it has four weeks of archive.

**Add-ons if you want them:** [Session 11, Influencer Scout](session-11-influencer-scout.md) and [Session 12, Telegram Bot](session-12-telegram.md).

**When you are ready for more tools:** [`resources.md`](resources.md), and read it before installing anything.
