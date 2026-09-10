# Session 2, Skills

**Time:** 90 minutes
**Primitive:** Skills, reusable playbooks Claude loads on its own
**Teammates hired:** 02 Market Analyst, 03 Voice of Customer, and one you write yourself
**You walk out with:** two real reports in `my-work/`, and a skill in your own handwriting

---

## Before you start

- [ ] `CLAUDE.md` exists and passed its voice test in Session 1
- [ ] `brand-brain/reviews.md` has real reviews in it, or you have some ready to paste
- [ ] `brand-brain/competitors.md` names at least three competitors

---

## What this teaches

A skill is a folder with a `SKILL.md` file in it. The file has a description at the top and instructions below.

Claude reads every description when your project loads. When something you ask matches one, it loads that skill's instructions and follows them. You can also call one directly by typing its name after a slash.

**Why this matters more than it sounds.** Without skills, you get a good answer that you then have to re-explain next week. With skills, the method is written down. The same question next month runs the same playbook, reads the same files, applies the same safety checks, and saves to the same place.

You are not prompting. You are writing job descriptions.

---

## Steps

### 1. Look at a skill before you run one

In the prompt, type:

```
Show me .claude/skills/market-analyst/SKILL.md
```

Click the file path to open it in the file pane. Read the top four lines.

Notice the structure: a `name`, a `description` that lists the phrases that should trigger it, then numbered steps, then a section at the bottom called "How you work" that sets the standard. That shape is the whole trick. **The description decides when it runs. The steps decide what it does. The standard decides whether the output is any good.**

### 2. Run the Market Analyst

```
/market-analyst
```

It will read `CLAUDE.md`, then say back which competitors it is about to research, over what window, and where it will save. **It waits for you to confirm.** Change the list or the window here if you want.

Say go, and it researches each competitor across pricing, positioning, content, organic presence and paid activity, then writes to `my-work/market-analyst/<date>-intel-report.md`.

**While it runs, watch what it says it cannot see.** It will tell you if a competitor's site is unreachable or if it could not find ad activity. That honesty is the point. A competitor report that never says "I could not check this" is guessing.

### 3. Read the report properly

Open the file. Go straight to two sections:

- **Where they beat us.** This is the one that stings and the one that is useful.
- **What only you can answer.** Two or three questions that would sharpen the next run. Answer them into `brand-brain/competitors.md` and the next run is better.

### 4. Run the Voice of Customer

```
/voice-of-customer
```

It asks where your customer text is. **Point it at your reviews file** by typing `@brand-brain/reviews.md`, or paste text straight into the chat.

It will count what it received and tell you honestly whether that is enough:

> "Under 30 messages, treat these as signals rather than patterns. Fifty or more makes the next run much sharper."

Then it confirms the run and waits. Say go.

It clusters five to eight themes with real counts, cuts sentiment three ways, builds two or three persona cards from the customers actually in your data, and saves to `my-work/voice-of-customer/`.

### 5. Read the one section that matters most

Open the report and find **"Where the data disagrees with your profile"**.

This is the most valuable page in the session. It lists every place your customers contradict what you believe about them. Founders are wrong about their own customers constantly, and this is the cheapest way to find out where.

**Take at least one finding from it back into `CLAUDE.md`.** Run `/brand-brain --rebuild` and update Section 5.

### 6. Write your own skill

This is the part that makes the rest of the weekend yours.

In the prompt, type:

```
I want to write my own skill called write-in-brand-voice. It should write or rewrite any customer-facing copy in my brand's voice: emails, captions, product blurbs, WhatsApp replies. It must read CLAUDE.md Section 7 for the voice rules and 3 to 5 matching samples from brand-brain/voice-dna/ before writing anything. Create .claude/skills/write-in-brand-voice/SKILL.md. Ask me questions about my voice before you write it, do not guess.
```

Answer its questions. When it saves the file, **read it and edit it yourself.** Change a line. Add a rule it missed. It is your skill.

Then test it:

```
/write-in-brand-voice write a two line note for the card that goes in the box
```

If it does not sound like you, open the SKILL.md and fix the rule that let it through. That loop, run, judge, edit the file, is the whole skill of writing skills.

**A worked version:** [`examples/the-paan-legacy/authored-skills/write-in-brand-voice.SKILL.md`](examples/the-paan-legacy/authored-skills/write-in-brand-voice.SKILL.md). Read it after you write yours, not before.

---

## Check it worked

- [ ] `my-work/market-analyst/` has a dated intel report
- [ ] `my-work/voice-of-customer/` has a dated VoC report
- [ ] You answered at least one "what only you can answer" question back into `brand-brain/`
- [ ] `.claude/skills/write-in-brand-voice/SKILL.md` exists and you edited it by hand
- [ ] Typing `/` now shows `write-in-brand-voice` in the list

---

## If it breaks

**The skill did not trigger when I described the job in plain English.**
Its `description` does not carry the words you used. Open the SKILL.md and add your phrasing to the description line. That is the fix, every time.

**Voice of Customer says my sample is too small.**
It will still run, it just labels the output as signals rather than patterns. Believe it. Go and export your full review set before the next run.

**The Market Analyst could not reach a competitor's site.**
It will say so in the report and mark the price as unverified. That is correct behaviour, not a failure. Check that one price by hand and paste it into `brand-brain/competitors.md`.

**My new skill runs but ignores my voice rules.**
It is not reading `CLAUDE.md` early enough. Open the SKILL.md and make step 1 explicitly "read CLAUDE.md Section 7 and 3 to 5 samples from brand-brain/voice-dna/ before writing a word".

---

## Take-home

Run `/market-analyst` again in a week with the same competitor set. The second report is where the value is, because it can tell you what moved.

**Next:** [Session 3, Connectors](session-3-mcps.md)
