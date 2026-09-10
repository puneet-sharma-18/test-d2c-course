# Session 1, Brand Brain

**Time:** 75 minutes
**Primitive:** `CLAUDE.md`, a persistent project profile
**Teammate hired:** 01, Brand Brain
**You walk out with:** `CLAUDE.md` at the repo root, filled in your voice, with a voice test scored 4 or better

---

## Before you start

- [ ] Session 0 done, `/` shows your roster
- [ ] `brand-brain/` exists at the repo root, however empty
- [ ] 75 uninterrupted minutes. This is the one session you cannot rush, because every other teammate reads its output

---

## What this teaches

`CLAUDE.md` is a file at the root of your project that Claude reads **before every single thing it does**, automatically, without you asking.

That is the whole idea. Instead of re-explaining your brand at the top of every conversation, you write it down once. Every teammate for the rest of the weekend inherits it.

It is the highest leverage file you will ever write for your brand. It is also the one most founders rush, and you can tell immediately in Session 4 when the content comes out sounding like a template.

## Pick your path

Two skills do this job. They differ only in where they start.

| Skill | Start here if |
|---|---|
| `/brand-brain` | You filled in some of `brand-brain/`. It reads your files first, then asks only about gaps. |
| `/interview-me` | You arrived cold. It asks you everything, section by section, and writes from your answers. |

Most founders should run `/brand-brain`. It handles both cases: share a file when you have one, talk it through when you do not.

---

## Steps

### 1. Start the session

Type into the prompt box:

```
/brand-brain
```

It will open by explaining what you are about to build together and ask if you are ready. Say yes.

### 2. Answer the persona questions

Four short ones: your name, your role, the brand name, and who you are in one line.

**On that last one, resist the pitch.** If you type "India's finest D2C gourmet brand" it will push back and ask what you would say to a friend at a wedding. The honest version, "I sold my family's paan shop in Kanpur to build this", is worth ten times the polished one, because it is the sentence every later teammate writes from.

### 3. Watch the demo

It shows you the same fake product launch caption twice: once with no brand profile, once as if it already had yours. That contrast is the whole reason this session exists. Then it asks you to say go.

### 4. Answer the two structure questions

Single brand or house of brands. Online only or omnichannel.

**Be honest on the second one.** If franchise, wholesale, quick commerce or store sales are more than roughly a tenth of your revenue, say so. It changes how Sections 2 and 7 get written, and a teammate that thinks you are online only will write you a Diwali plan that ignores your three stores.

### 5. Walk the eight topics

For each one it asks the same thing: **got a file for this, or should we talk it through?**

| # | Topic | Goes into |
|---|---|---|
| 1 | Positioning and anti-positioning | Section 3, Story |
| 2 | Products | Section 4 |
| 3 | Nominated focus SKUs | An aside, used in Sessions 3 and 7 |
| 4 | Competitors | Section 6 |
| 5 | Reviews | Section 5, Customer |
| 6 | Unit economics | Section 7, Channels |
| 7 | Ads | Section 7, Ad angles |
| 8 | Voice DNA | Section 7, Voice rules and compliance |

**How to share a file:** drag it onto the prompt box, or type `@` and start typing the filename. Both work. `@brand-brain/reviews.md` is the fastest way.

**Three commands you can use at any point:**

- `draft it` — it proposes something plausible from what it already knows, you correct it
- `example` — it shows one personalised example of a good answer
- `skip` — that section becomes a TODO you can fill later

### 6. Spend real time on Topic 8

Topic 8 is voice and compliance, and it is the one that protects every other teammate's output for the rest of the weekend.

It will ask for phrases that are quintessentially you, words you would never use, your reading level, and **any regulated claims for your category**. FSSAI for food, CDSCO for cosmetics, Ayush for wellness, plus anything your category has been pulled up on.

Do not rush this. A teammate that does not know your claim wall will eventually write "boosts immunity" on a product page, and that is a takedown, not a typo.

### 7. Take the voice test

Before saving, it writes a three line Instagram caption for a made up product drop, using nothing but the profile you just built. Then it asks you to score it 1 to 5.

**Score it honestly.** 3 means a customer who knows your brand would notice something is off. If you score 3 or below it asks which section to tighten and tries again, twice at most.

**Do not accept a 3 to be polite.** Every teammate for the next two days writes from these voice rules.

### 8. Save

It shows you the whole file in one block. Read it. Then say yes and it writes `CLAUDE.md` to the repo root.

---

## Check it worked

- [ ] `CLAUDE.md` exists at the repo root. Click it in the chat to open it in the file pane.
- [ ] Sections 1 to 7 are filled with your real answers, not brackets
- [ ] Section 7 carries an ALWAYS list, a NEVER list, a reading level and your compliance wall
- [ ] The voice test scored 4 or 5
- [ ] Anything you skipped is marked `TODO` with a note on what is missing

**The real test.** Start a new prompt and type:

```
Write me a two line Instagram caption announcing that we are back in stock.
```

You did not name a product, a tone or a rule. It should still sound like your brand. That is `CLAUDE.md` working.

---

## If it breaks

**It keeps writing marketing filler back at me.**
Push back once, hard: "that is the pitch deck line, what would you say to a friend?" If it still reads generic, your voice-dna folder is thin. Paste two real things you wrote directly into the chat and ask it to re-extract.

**It invented a fact about my brand.**
Tell it immediately and name the line. It is instructed not to invent, so this means it inferred from something ambiguous. Correct it and it will re-show the section.

**I ran out of time at topic 5.**
Say `skip` through the rest and save. The unfinished sections are marked TODO. Come back with `/brand-brain --rebuild`, which touches only the TODO sections and leaves the rest alone.

**I want to start over.**
`/brand-brain --rebuild` to fix sections. To genuinely start again, rename the existing file to `CLAUDE-old.md` first so you can compare.

---

## What good looks like

Open the filled profile in whichever brand is closer to yours: [`examples/the-paan-legacy/CLAUDE.md`](examples/the-paan-legacy/CLAUDE.md) for food under FSSAI, or [`examples/little-lab/CLAUDE.md`](examples/little-lab/CLAUDE.md) for cosmetics under CDSCO.

Read Section 7 in particular. Notice that the voice rules are not adjectives, they are examples: "name the thing, do not adjective it", followed by a real line from the brand's own product page. Notice the claim wall is a table with a named risk at the bottom. That is the standard.

Then open the matching [`brand-brain/`](examples/the-paan-legacy/brand-brain/) folder to see the input files that produced it. Read both brands' Section 7 side by side if you have five minutes: same framework, two completely different compliance regimes, and you can see exactly where the difference comes from.

---

## Take-home

Re-run `/brand-brain --rebuild` after Session 2. The Market Analyst and Voice of Customer reports will have found things about your customers and competitors that belong in the profile. Brand Brain gets richer every week you feed it.

**Next:** [Session 2, Skills](session-2-skills.md)
