# Session 12, Telegram Bot (add-on)

**Time:** 45 minutes
**Primitive:** none new, this is your existing skills reached from a phone
**You walk out with:** a Telegram bot that answers in your brand voice, from a DM

---

## Read this first

**This add-on needs the Claude Code CLI, not just the desktop app.**

Everything else in this bootcamp runs in the desktop app. This one does not, and it is worth being clear about why rather than discovering it halfway through.

The bot is a small background process. When a Telegram message arrives, it runs Claude as a subprocess and sends the answer back. A background process cannot drive a desktop application, so it calls the command line version instead.

**What that means for you.** You need to install one more thing and use a terminal for about ten minutes. If that is not something you want to do today, skip this session. Nothing else in the bootcamp depends on it.

---

## Before you start

- [ ] Session 2 done, and `/write-in-brand-voice` working in the desktop app
- [ ] `CLAUDE.md` filled
- [ ] **Node.js** installed. Check at [nodejs.org](https://nodejs.org), take the LTS version.
- [ ] **The Claude Code CLI** installed and signed in. Follow [code.claude.com/docs](https://code.claude.com/docs).
- [ ] A Telegram account

---

## What this teaches

The bot is about a hundred lines and it does one thing: forward a message to Claude, send the answer back.

**It does not know what any of your skills do.** There is no command list in it, no prompt for `/write-in-brand-voice`, no routing logic. It just forwards.

That is the whole lesson. **All the intelligence lives in your skills, so every new skill you write lands on your phone the moment you save it**, with no bot code to update. If the bot ever breaks, it is short enough to read in one sitting.

---

## Steps

### 1. Create the bot

In Telegram, message **@BotFather**. Send `/newbot`, give it a name and a username.

It replies with a token that looks like `1234567890:AA...`. **That token is a password.** Anyone who has it controls the bot.

### 2. Store the token safely

At the repo root, create a file called `.env` and put the token in it:

```
TELEGRAM_BOT_TOKEN=your-token-here
```

`.env` is already in `.gitignore`, so it never gets committed. Check that before you continue:

```
Confirm that .env is gitignored and will never be committed.
```

### 3. Install and start

Open Terminal on Mac or Git Bash on Windows:

```bash
cd ~/d2c-insider-ai-bootcamp/telegram-bot
npm install
node ai_team_bot.js
```

Leave that window open. The bot runs only while it is running.

### 4. Talk to it

Find your bot in Telegram by the username you chose and send it a message:

```
write a two line caption announcing we are back in stock
```

It should answer in your brand voice, because Claude reads your `CLAUDE.md` before answering.

Then try a skill by name:

```
/write-in-brand-voice reply to a customer who says their order arrived late
```

### 5. Understand what just happened

Your phone sent text to a process on your laptop, which ran Claude in your project folder, which read your `CLAUDE.md` and your voice samples and your skills, and sent the answer back.

**Nothing about the bot is brand-specific.** Point it at a different folder and it becomes a different brand's assistant.

### 6. Know the limits

Be honest with yourself about what this is:

- **It runs only while your laptop is on and that terminal window is open.** Close the laptop and the bot is dead until you start it again.
- **Anyone who finds your bot can use it**, unless you add a check on the sender's Telegram ID. Ask Claude to add one before you share the bot's name with anybody.
- **It is a demo, not infrastructure.** Putting it on a server so it runs permanently is a real piece of work and outside this bootcamp.

---

## Check it worked

- [ ] The bot replies to a plain English message
- [ ] The reply sounds like your brand rather than generic
- [ ] Calling a skill by name works
- [ ] `.env` holds the token and is confirmed gitignored
- [ ] You can explain why every new skill appears on your phone for free

---

## If it breaks

**The bot does not reply at all.**
The process stopped. Look at the terminal window for an error. The usual cause is a missing or mistyped token.

**It replies but sounds generic.**
It is running in the wrong folder, so there is no `CLAUDE.md` to read. Start it from inside the bootcamp folder.

**"claude: command not found".**
The CLI is not installed or not on your PATH. That is separate from the desktop app. Install it from [code.claude.com/docs](https://code.claude.com/docs).

**Replies are slow.**
Expected. Each message is a fresh Claude run reading your whole brand profile. Ten to thirty seconds is normal.

**Formatting looks broken in Telegram.**
Telegram's markdown is stricter than most. Ask Claude to strip formatting to plain text before sending.

---

## Take-home

Add the sender check. Then every skill you write for the rest of the year is on your phone the day you write it, at no extra cost.

**Back to:** [Student Handbook](student-handbook.md)
