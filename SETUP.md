# IT Audit Jeopardy — Setup Guide

## What you need (all free, no credit card)
- A GitHub account (free) → hosts the game website
- A Supabase account (free) → powers real-time buzzing

---

## STEP 1 — Create a free Supabase project

1. Go to https://supabase.com and click **Start your project**
2. Sign up with GitHub or email (free)
3. Click **New Project**
4. Fill in:
   - **Name**: jeopardy (or anything)
   - **Database Password**: make one up and save it somewhere
   - **Region**: pick the closest to you
5. Click **Create new project** — wait ~1 minute for it to set up
6. Once ready, click **Project Settings** (gear icon, bottom left)
7. Click **API** in the left menu
8. Copy two things:
   - **Project URL** — looks like `https://abcdefghij.supabase.co`
   - **anon / public key** — a long string starting with `eyJ...`

That's it for Supabase! You do NOT need to create any tables — the real-time channel works out of the box.

---

## STEP 2 — Put your files on GitHub Pages

1. Go to https://github.com and sign in (or create a free account)
2. Click the **+** icon → **New repository**
3. Name it: `jeopardy` (or anything you like)
4. Set it to **Public**
5. Click **Create repository**
6. On the next page, click **uploading an existing file**
7. Drag and drop these 3 files:
   - `index.html`
   - `buzz.html`
   - `SETUP.md`
8. Click **Commit changes**
9. Now go to **Settings** → **Pages** (left sidebar)
10. Under **Branch**, select `main` and click **Save**
11. Wait ~60 seconds, then your site is live at:
    `https://YOUR-GITHUB-USERNAME.github.io/jeopardy/`

---

## STEP 3 — Play the game!

### Teacher setup (you do this once before class):
1. Open `https://YOUR-GITHUB-USERNAME.github.io/jeopardy/` on your projected computer
2. Paste in your Supabase **Project URL** and **Anon Key**
3. Set a **Room Name** (e.g. `room1`) — students need to use the same name
4. Click **Launch Teacher Board**
5. Click **📱 Student Link** to see the URL to share with students

### Students join:
1. Students open `https://YOUR-GITHUB-USERNAME.github.io/jeopardy/buzz.html` on their phone or laptop
2. They enter the same Supabase URL, Key, and Room Name
3. They select their Group Number
4. Click **Join Game**

> **Tip:** To make it even easier for students, add the Supabase URL, key, and room as URL parameters so they don't have to type them:
> `buzz.html?room=room1&url=YOUR_SUPABASE_URL&key=YOUR_ANON_KEY`
> Students only need to pick their group number!

### Playing:
- Teacher clicks a dollar amount on the board → question appears
- Students race to hit the big **BUZZ!** button
- First buzz lights up on the teacher screen instantly
- Teacher clicks **Correct** or **Wrong** → points update
- Click **Show Answer** to reveal the correct choice
- Used questions show ✓ on the board

---

## Tips

- **Edit Questions**: Click "✏️ Edit Questions" on the teacher board anytime to update any question
- **Reset between rounds**: "↺ Reset Scores" keeps the board, "🆕 New Game" resets everything
- **Multiple classes**: Use a different Room Name for each class period (e.g. `period1`, `period2`)
- **Student link shortcut**: Once you know your URL/key/room, bookmark the full buzz.html URL with parameters for each class

---

## Troubleshooting

**Buzz button not working / not showing on teacher screen:**
- Make sure students and teacher are using the exact same Room Name
- Make sure Supabase URL and Key are entered correctly (no extra spaces)
- Check that your Supabase project is active (free projects pause after 1 week of inactivity — just log in to reactivate)

**GitHub Pages not loading:**
- Make sure the repository is set to Public
- Wait 2–3 minutes after enabling Pages for it to go live

**Supabase free tier limits:**
- 500MB database, 2GB bandwidth/month — more than enough for classroom use
- Projects pause after 1 week of inactivity on free tier — log into Supabase to wake it up before class
