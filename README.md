# ✦ The Notebook — Creative Writing Suite

A personal writing app with Google Drive sync. Works on any device.

---

## Setup (one time)

### 1. Deploy to Vercel
- Push this repo to GitHub (private)
- Go to vercel.com → New Project → import this repo
- Deploy — Vercel will give you a URL like `the-notebook-xyz.vercel.app`

### 2. Google Cloud Console
Go to [console.cloud.google.com](https://console.cloud.google.com)

1. Create a new project (e.g. "The Notebook")
2. **Enable APIs & Services → Library → Google Drive API**
3. **Credentials → Create Credentials → API Key** — copy it
4. **Credentials → Create Credentials → OAuth 2.0 Client ID**
   - Application type: **Web application**
   - Authorized JavaScript origins: add your Vercel URL (e.g. `https://the-notebook-xyz.vercel.app`)
   - Authorized redirect URIs: same URL
   - Create — copy the Client ID

### 3. Add credentials to the app
Open `index.html` and find this section near the top of the `<script>`:

```js
const GOOGLE_CLIENT_ID = 'YOUR_CLIENT_ID.apps.googleusercontent.com';
const GOOGLE_API_KEY   = 'YOUR_API_KEY';
```

Replace with your actual values, save, and push to GitHub. Vercel auto-deploys.

---

## Using the app

- Open your Vercel URL on any device
- Sign in with your Google account on first load
- Your project auto-saves to a file called `notebook-project.json` inside a folder called `The Notebook App` in your Drive
- Any device you open the app on will pull the latest version automatically

---

## Features
- 🗺 Planning — logline, genre, tone, act structure, beat sheet
- 🃏 Storyboard — drag-and-drop scene cards
- 📺 Episodes / Chapters — toggle between series and book mode
- 🎭 Characters — full dashboards with photo + inspiration boards
- 📍 Locations — same treatment with scene tracking
- ✍️ Write — screenplay, prose, and Apple Pencil modes
- 🌙 Dark/light paper toggle
- ☁️ Auto-sync to Google Drive
