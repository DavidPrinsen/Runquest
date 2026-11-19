# Runquest

A simple running coach for people who just started running. Pick a goal (5K, 10K, half marathon or marathon), follow a weekly plan that matches your level, save each run, and level up as you go.

Everything lives in one file, `index.html`. There is nothing to install and no server to run.

## What the app does

- Builds a weekly plan from your goal, race day, age and level
- Shows today's run in plain words, with a short tip
- Saves your runs and adapts next week's plan
- Gives XP and a level for every run, with skins and Prestige at level 30
- Imports runs from a Garmin file (CSV, GPX or TCX)
- Saves your data on your own device

Only inside Claude: scanning a screenshot, the AI plan adjuster, and the social feed. On Render these are hidden automatically.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app. The name must be exactly this. |
| `icon.png` | The icon for the iPhone Home Screen |
| `README.md` | This guide |

## Step 1: Put the files on GitHub

GitHub stores your files. Render then reads them from there.

1. Go to **github.com** and tap **Sign up** (or **Sign in**).
2. Tap the **+** at the top right, then **New repository**.
3. Repository name: `runquest`. Choose **Public**. Leave "Add a README file" **unticked**. Tap **Create repository**.
4. On the new page tap **uploading an existing file**.
   - On an iPhone this link can be missing. In Safari tap **aA** in the address bar, then **Request Desktop Website**, and reload.
5. Add the three files: `index.html`, `icon.png`, `README.md`. Wait until all three are listed.
6. Scroll down and tap **Commit changes**.
7. Check the repository page: you should see all three files in the top folder, not inside another folder.

## Step 2: Publish it with Render

1. Go to **render.com** and tap **Get Started**. Choose **Sign in with GitHub** and allow it.
2. Tap **New +**, then **Static Site**.
3. Connect your GitHub account if asked, find the `runquest` repository and tap **Connect**.
4. Fill in the form:
   - **Name:** `runquest` (this becomes part of your link)
   - **Branch:** `main`
   - **Build Command:** leave empty (or type `echo ok`)
   - **Publish Directory:** `.` (one single dot)
5. Tap **Create Static Site**.
6. Wait about a minute until it says **Live**.
7. Your link is at the top, like `https://runquest.onrender.com`. Open it to check.

Static sites are free on Render. Check Render's pricing page for the current limits.

## Step 3: Put it on your iPhone like an app

1. Open your Render link in **Safari**.
2. Tap the **Share** button, then **Add to Home Screen**, then **Add**.
3. Open RunQuest from the Home Screen. It runs full screen.

## Step 4: Change the app later

1. On GitHub open `index.html`, tap the pencil icon, and make your change (or replace the file with **Add file > Upload files**).
2. Tap **Commit changes**.
3. Render notices and publishes the new version by itself in about a minute.

## If something goes wrong

- **404 or blank page:** `index.html` must be in the top folder and named exactly `index.html`. Publish Directory must be `.`
- **Still the old version:** reload the page. In Render open your site, then **Manual Deploy > Clear build cache & deploy**.
- **My runs disappeared:** runs are saved per browser and per device. Safari and the Home Screen app keep separate data, and clearing website data deletes them.
- **Render asks for a card:** a Static Site should not. Make sure you chose **Static Site**, not Web Service.
