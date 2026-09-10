# Session 4, Content Lead

**Time:** 90 minutes
**Primitive:** Subagents, teammates that run in their own context
**Teammate hired:** 04, Content Lead
**You walk out with:** a 30 day calendar, drafted content pieces, first marketplace listings, and every safety flag they raised

---

## Before you start

- [ ] `CLAUDE.md` filled, voice test passed
- [ ] A Market Analyst report and a Voice of Customer report in `my-work/`
- [ ] Ideally the live-data VoC report from Session 3

The Content Lead refuses to run without the two reports. That is deliberate: **topics come from real customer themes or they do not exist.** A content calendar invented from nothing is the thing this whole bootcamp is built to stop you shipping.

---

## What this teaches

A skill runs inside your conversation. Everything it reads and writes fills up the same session you are sitting in.

A **subagent** is different. It gets its own context, does a large job, and hands back a summary. The forty files it read to get there never touch your session.

**Why that matters for you specifically.** A 30 day calendar plus a batch of pieces plus marketplace listings is far too much work to do in a chat without running out of room. A subagent does it in its own space and comes back with one message and a pile of files.

The trade: you cannot talk to it mid-run. You brief it once, fully, and it goes. So the brief has to carry everything.

---

## Steps

### 1. Look at the subagent definition

```
Show me .claude/agents/content-lead.md
```

Open it. Notice the top: a `description` saying when to use it, and a `tools` line listing exactly what it is allowed to touch. Notice Step 0, where it sizes its own run, and Step 5, the seven-check safety pass.

**This is a job description, not a prompt.** That is the mental shift for the rest of the weekend.

### 2. Start it

You can call a subagent three ways. The simplest:

```
Use the content-lead agent to produce this month's content.
```

Or mention it directly with `@content-lead`.

**Watch the Tasks pane.** A row appears showing the agent running. Click it to watch the live transcript. This is worth doing once so that later, when the Performance Marketer fans out to several agents at once, you know what you are looking at.

### 3. Pick your scope

The Content Lead defaults to a **focused run**: the full 30 day calendar, five pieces, two marketplace listings.

That is the right choice in the room. If you want everything, say so in the brief:

```
Use the content-lead agent with FULL_RUN=yes to produce this month's content.
```

Full run is twenty pieces and ten listings. Save it for Sunday night.

### 4. Let it work

It reads `CLAUDE.md`, both reports, and any previous content index, then plans the calendar against a fixed weighting: 40 percent to your top two customer themes, 25 percent to the gap the Market Analyst found, 20 percent product, 15 percent brand story.

Then it drafts, runs the safety pass on every piece, and writes an index.

**It will take several minutes.** That is normal. Read your VoC report while you wait.

### 5. Read the index first, never the pieces

When it finishes, open `my-work/content-lead/<date>-index.md`.

The index is written for exactly this moment. It carries the top five reads: what ships first and why, the piece closest to your biggest customer theme, the one that attacks the competitive gap, the listing with the most upside, and anything flagged.

**Only then open individual pieces.** Founders who start by reading twenty drafts lose an hour and no signal.

### 6. Work the safety flags

Every piece that failed a check carries a `## SAFETY FLAGS` section naming the issue. The agent flags rather than fixes, on purpose, because a flagged piece you reject beats a takedown later.

Go through them and sort into three piles:

- **Blocking.** A missing FSSAI number, a gluten claim you cannot make, an invented statistic. Fix the underlying fact.
- **Yours to decide.** A claim that is true but you have no proof document for. Get the proof or cut the line.
- **Wrong.** It flagged something that is genuinely fine. Tell it, and tell it why, so the reasoning improves.

### 7. Ship one thing

Pick the piece the index says goes first. Read it once. Change one word so it is yours.

**Post it today.** Not because the piece is precious, but because a founder who ships one thing in the room ships the next twenty at home, and a founder who ships nothing has a folder.

---

## Check it worked

- [ ] `my-work/content-lead/<date>-calendar.md` covers 30 days, each row naming the theme it serves and the source it traces to
- [ ] `my-work/content-lead/pieces/` has drafts in it
- [ ] `my-work/content-lead/marketplace/` has listings
- [ ] `my-work/content-lead/<date>-index.md` exists and you read it before anything else
- [ ] You sorted every safety flag into fix, decide or dismiss
- [ ] One piece is scheduled or posted

---

## If it breaks

**It stopped and said a report is missing.**
Correct behaviour. Go back and run `/market-analyst` or `/voice-of-customer` first. It will not invent topics.

**Every piece sounds slightly generic.**
The problem is upstream in `CLAUDE.md`, not here. Check Section 7 carries real example phrases rather than adjectives, and that `brand-brain/voice-dna/` has real samples. Fix that, then re-run.

**It skipped a product entirely.**
Read the index section called "what I did not do". It usually explains itself: a SKU blocked on a decision, a seasonal angle out of window. That reasoning is often more useful than the pieces.

**The calendar has placeholder dates in it.**
It refuses to invent festival dates it cannot source. Fill them in yourself, then those rows are schedulable.

**It produced twenty pieces and I wanted five.**
`FULL_RUN=yes` got into the brief. Re-run without it.

---

## What good looks like

[`examples/the-paan-legacy/my-work/content-lead/`](examples/the-paan-legacy/my-work/content-lead/) and [`examples/little-lab/my-work/content-lead/`](examples/little-lab/my-work/content-lead/) each hold a complete run. Open the index first, exactly as you should with your own.

---

## Take-home

Run it monthly. Each run reads the previous index so it does not repeat last month. Feed it a fresh VoC report first and the calendar tracks what your customers are actually saying rather than what they said in September.

**Next:** [Session 5, Day 1 Integration](session-5-integration.md)
