# Session 0, Setup

**Time:** 30 minutes, do it before Saturday if you can
**Primitive:** none yet, this is plumbing
**You walk out with:** the Claude Code desktop app installed, this repo open inside it, and one successful run

---

## Before you start

- [ ] A Claude **Pro or Max** plan. Claude Code does not run on the free tier. Check at [claude.ai](https://claude.ai) under your account.
- [ ] A Mac or a Windows machine you can install software on.
- [ ] About 2 GB of free disk.

---

## 1. Install the app

Go to the desktop quickstart and download the installer for your machine:

**[code.claude.com/docs/en/desktop-quickstart](https://code.claude.com/docs/en/desktop-quickstart)**

**On Mac:** open the downloaded `.dmg` and drag Claude into Applications. Open it from Applications.

**On Windows:** run the downloaded `.exe`. It does not need admin rights.

> **Windows only, do this too.** Install **Git for Windows** from [git-scm.com/download/win](https://git-scm.com/download/win). Accept every default. Without it some tools in the app fall back to a weaker mode, and step 3 below will not work. Mac already has what it needs.

## 2. Sign in

Open the app. Sign in with the same Anthropic account your Pro or Max plan is on.

You will see three tabs at the top: **Chat**, **Cowork** and **Code**.

**Click Code.** Everything in this bootcamp happens in the Code tab. If you find yourself in Chat, you are in the wrong place and skills will not appear.

## 3. Get this repo onto your machine

The desktop app cannot clone from GitHub for you, so do it first.

**If you have Git** (Mac has it, Windows has it after step 1):

Open Terminal on Mac, or Git Bash on Windows, and run these two lines. This is the only time you touch a command line all weekend.

```bash
cd ~
git clone https://github.com/puneet-sharma-18/test-d2c-course.git d2c-insider-ai-bootcamp
```

**If that fails or you would rather not:** open the repo page on GitHub, click the green **Code** button, choose **Download ZIP**, and unzip it into your home folder. Rename the unzipped folder to `d2c-insider-ai-bootcamp`.

Either way you end up with a folder at `~/d2c-insider-ai-bootcamp` on Mac, or `C:\Users\you\d2c-insider-ai-bootcamp` on Windows.

> **Do not put it in iCloud Drive, OneDrive or Dropbox.** Sync services rewrite files under the app while it is working. Put it directly in your home folder.

## 4. Open the folder in the app

In the **Code** tab, click **Select folder** and choose `d2c-insider-ai-bootcamp`.

The app will ask you to trust the folder. Say yes. Trust is what allows the skills in `.claude/skills/` to load, so if you decline, none of your teammates will exist.

## 5. Meet your teammates

Click into the prompt box and type a single forward slash:

```
/
```

A list appears. You should see `brand-brain`, `interview-me`, `market-analyst`, `voice-of-customer`, `ops-manager` and more. **That list is your roster.** Every one of those is a teammate defined in a file inside `.claude/skills/`.

If the list is empty or has none of those names, jump to troubleshooting at the bottom.

Press Escape to close the list without running anything.

## 6. Your first run

Type this into the prompt box and send it:

```
Read README.md and examples/the-paan-legacy/CLAUDE.md, then tell me in five lines what this repo is for and what a finished CLAUDE.md looks like.
```

Watch what happens. Claude will ask permission to read files, then answer. Two things to notice:

- **The permission card.** Claude asks before it touches anything. You can choose "Allow once" or "Always allow". For reading files inside this folder, "Always allow" is safe and will save you a hundred clicks this weekend.
- **The file paths in the answer.** Click one. It opens in a file pane inside the app. You never need Finder or Explorer to read your teammates' work.

## 7. Set your permission mode

Find the permission mode selector near the prompt box. There are four:

| Mode | What it does | Use it when |
|---|---|---|
| **Manual** | Asks before every edit, shows you a diff | You are nervous, or reviewing someone else's work |
| **Accept edits** | Auto-approves file edits and safe commands | **Use this for the bootcamp** |
| **Plan** | Reads and proposes, never edits | You want a plan before any change |
| **Auto** | Fewer prompts, a safety classifier watches | Later, once you trust the setup |

**Set it to Accept edits** for the weekend. Your teammates write a lot of files and approving each one individually will eat your session.

## 8. Copy the brand-brain template

In the app prompt, type:

```
Copy the templates/brand-brain folder to the repo root as brand-brain/, keeping every file.
```

Then open `brand-brain/README.md` and start filling the files with your real data. This is the pre-work. Whatever you get done before Session 1 makes every session after it better.

---

## Check it worked

You are ready for Session 1 when all five are true:

- [ ] The app is open on the **Code** tab
- [ ] The folder `d2c-insider-ai-bootcamp` is selected and trusted
- [ ] Typing `/` shows at least ten teammate names
- [ ] Your first run answered and you clicked a file path to read something
- [ ] A `brand-brain/` folder exists at the repo root

---

## If it breaks

**The `/` list is empty, or missing teammates.**
The folder is not trusted, or you opened the wrong folder. Check the folder path shown in the app is the one containing `.claude/`. Re-select the folder and accept the trust prompt.

**"Claude Code requires a paid plan".**
Free tier will not work. Pro is enough for everything in Default scope.

**Windows: tools fail or commands do nothing.**
Git for Windows is missing. Install it from [git-scm.com/download/win](https://git-scm.com/download/win), then quit and reopen the app.

**Files keep reverting, or the app says a file changed underneath it.**
The repo is inside iCloud, OneDrive or Dropbox. Move it to your home folder and re-select it.

**The app is slow or a run stops halfway.**
Check the usage ring next to the model picker. If you are near your limit, wait for the reset or switch to Default scope for the session.

**Anything else.** [`references/module-0-setup/troubleshooting.md`](references/module-0-setup/troubleshooting.md).

---

## Take-home

Fill in as much of `brand-brain/` as you can before Saturday. In priority order:

1. `voice-dna/`, five things you actually wrote
2. `reviews.md`, as many real reviews as you can paste, including the bad ones
3. `positioning.md`, one honest paragraph
4. `products.csv`, your real SKUs and numbers
5. everything else

**Next:** [Session 1, Brand Brain](session-1-brand-brain.md)
