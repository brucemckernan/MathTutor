# MathTutor — iPad Travel Guide

A self-contained reference for working through math exercises while away from your Mac Studio.

---

## Apps You Need (install before leaving)

| App | Where | Cost | Purpose |
|-----|-------|------|---------|
| **Carnets** | App Store | Free | Runs Jupyter notebooks offline on iPad |
| **Working Copy** | App Store | Free + $20 unlock | Git client — syncs notebooks to/from GitHub |

> **Working Copy note:** The free version lets you download (pull). The $20 "Pro Unlock" (one-time, in-app purchase) enables uploading (push). You need this to send your completed work back to GitHub. Buy it when you install the app.

---

## One-Time Setup (do this at home before your first trip)

### Step 1 — Install and link Working Copy to GitHub

1. Open **Working Copy** on iPad
2. Tap the **person icon** (top right) → **Hosting Providers** → **GitHub**
3. Tap **Sign In** and log in with your GitHub account (`brucemckernan`)
4. Approve the access request

### Step 2 — Clone the MathTutor repository

1. In Working Copy, tap the **+** button (top right)
2. Tap **Clone Repository**
3. Your GitHub repos will appear — tap **MathTutor**
4. Tap **Clone** — Working Copy downloads all the notebooks to your iPad
5. You will see `MathTutor` appear in the Working Copy sidebar

### Step 3 — Connect Carnets to Working Copy's files

1. Open **Carnets**
2. Tap the **folder icon** to open the file browser
3. Tap **Browse** (bottom of screen) → **On My iPad** → look for **Working Copy**
4. If Working Copy doesn't appear, go to iPad **Settings → Carnets → Files → enable Working Copy**
5. You should now see `MathTutor` and its notebooks listed inside Carnets

> You only need to do this setup once. The connection persists across trips.

---

## Before You Leave Home (each trip)

Do this on your **Mac Studio** the day before you travel:

```bash
cd /Users/bruce/Projects/MathTutor
git pull          # make sure you have the latest
git status        # confirm nothing is pending
```

Then on your **iPad**:

1. Open **Working Copy**
2. Tap **MathTutor** in the sidebar
3. Tap the **pull icon** (downward arrow, top right) → **Pull**
4. Working Copy confirms "Already up to date" or downloads any new files
5. Your iPad now has the latest notebooks ready for offline use

---

## Working Through Exercises Offline (in Carnets)

1. Open **Carnets** on your iPad
2. Navigate to **Working Copy → MathTutor**
3. Tap the session notebook you want to work on (e.g. `session_01_diagnostic.ipynb`)
4. Carnets opens it exactly like JupyterLab on your Mac
5. Write your answers in the markdown cells below each question
6. Run Python code cells normally with the ▶ button
7. **Save frequently:** tap the save icon or use the keyboard shortcut

> Carnets saves changes directly back into the Working Copy folder. You do not need to export or copy anything — Working Copy sees the changes automatically.

---

## Submitting Your Work to Claude for Feedback (needs wifi)

When you have internet access and want feedback on your answers:

### Step 1 — Export your notebook from Carnets

1. In Carnets, with your notebook open, tap the **share icon** (top right)
2. Tap **Export as HTML** — this creates a readable version of your notebook
3. Tap **Save to Files** → save it anywhere convenient (e.g. iCloud Drive)

### Step 2 — Submit to Claude.ai

1. Open **Safari** and go to `claude.ai`
2. Start a new conversation
3. Tap the **paperclip / attachment icon** in the message bar
4. Navigate to the HTML file you just exported and attach it
5. Type your request, for example:

   > *"This is my MathTutor session notebook. Please review my answers to questions A2, A3 and B1, give me detailed feedback on my reasoning, point out any errors, and confirm correct working. Format your response as you normally would in our tutoring sessions."*

6. Claude will read your notebook and provide feedback in the chat

### Step 3 — Save the feedback

1. **Copy Claude's feedback** from the chat (tap and hold → Select All → Copy)
2. Open the **Notes** app on your iPad
3. Create a new note titled e.g. `Session 01 Feedback — travel`
4. Paste Claude's feedback in
5. When back home, you and Claude will convert this into the proper `_feedback.ipynb` format

> **Tip:** If the conversation is long, you can continue it in later sessions. Claude.ai preserves conversation history so you can say *"continuing from earlier — here are my answers to B2 and B3"* in a follow-up message.

---

## Committing Your Completed Work to GitHub (needs wifi)

Once you have finished a study session and want to save your work permanently:

1. Open **Working Copy**
2. Tap **MathTutor** in the sidebar — you will see changed files highlighted in orange/green
3. Tap the changed notebook file (e.g. `session_01_diagnostic.ipynb`)
4. You can review what changed if you like, then tap **back** to the repository view
5. Tap the **tick/checkmark icon** (top right) to open the commit screen
6. In the **Commit Message** box, type something descriptive, e.g.:
   > `Complete session 01 answers — A2, A3, B1 done`
7. Tap **Commit** — your changes are saved locally
8. Tap the **push icon** (upward arrow) → **Push** — your work uploads to GitHub

> **If push fails:** You need the Working Copy Pro Unlock ($20). See the Apps table at the top of this guide.

---

## Returning Home — Syncing Back to Mac Studio

When you get back, do this **before** opening anything in JupyterLab on your Mac:

```bash
cd /Users/bruce/Projects/MathTutor
git pull
```

This downloads everything you committed from the iPad. Your updated notebooks will be there.

Then continue the normal workflow:

1. Open JupyterLab on Mac Studio
2. Review your travel answers in the session notebook
3. Start Claude Code and ask it to write the `_feedback.ipynb` — paste or describe your answers as usual
4. Claude writes feedback into the feedback notebook
5. Commit everything from Mac:

```bash
git add .
git commit -m "Add session 01 feedback after travel"
git push
```

---

## Quick Reference Card

| Situation | What to do |
|-----------|------------|
| Before leaving | `git pull` on Mac, then Pull in Working Copy on iPad |
| Working offline | Open notebook in Carnets via Working Copy folder |
| Want feedback | Export as HTML from Carnets → attach to claude.ai |
| Save progress | Commit + Push in Working Copy |
| Back home | `git pull` on Mac Studio **first**, then open JupyterLab |
| Conflict warning | Don't edit the same notebook on Mac and iPad without syncing in between |

---

## If Something Goes Wrong

**"Working Copy says there's a conflict"**
> This means the same file was changed on both Mac and iPad without syncing. Open Working Copy, tap the file, and tap **Resolve**. Choose "Keep Mine" (iPad version) or "Keep Theirs" (Mac version), whichever has the work you want to keep. When in doubt, keep the iPad version and manually re-apply any Mac changes afterwards.

**"Carnets can't find my notebooks"**
> Go to Working Copy → MathTutor → pull to make sure files are there. Then in Carnets tap Browse → On My iPad → Working Copy → MathTutor.

**"Claude.ai won't accept the HTML file"**
> As an alternative, in Carnets tap Share → **Export as Markdown** or just copy the text content of your answer cells, then paste directly into the Claude.ai message box.

**"I forgot to pull before I left and my iPad is out of date"**
> As long as you only add new answers (don't delete or rewrite existing content), this is usually fine. Commit your work from iPad, then on Mac do `git pull` — git will merge cleanly. Only a problem if the same part of a file was changed in both places.
