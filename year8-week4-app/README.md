# Year 8 Maths Homework — Week 4 (app)

An installable, offline-capable web app (PWA) version of
`IGS_Durham_Year8_Homework_Week4.html`.

## What the app adds
- **Install to home screen / desktop** — "⬇ Install app" button (Chrome/Edge/Android);
  on iPhone/iPad use Share → *Add to Home Screen*.
- **Works offline** after the first visit (service worker caches the app).
- **Autosave** — name, answers, challenge answers and notes are kept on the device
  until *Start again* is pressed.
- Friendlier marking: accepts `−`/`-`, `x`/`*`/`×`, `/`/`÷` and a leading `£`.
- Phone-friendly results layout.

## Running it
Service workers need `https://` (or `localhost`), so host the folder, e.g. with
GitHub Pages (Settings → Pages → deploy from this branch), then open
`/year8-week4-app/`. For a local test: `python3 -m http.server` in this folder and
visit `http://localhost:8000`. Opening `index.html` directly still works, just
without install/offline.

## Submissions
`FORMSPREE_URL` and `SHEET_URL` near the top of the `<script>` in `index.html` are
still placeholders (`YOUR_FORM_ID`, `YOUR_SCRIPT_ID`) — fill them in for
"Submit to Mr Gascoigne" to work.

When you change `index.html`, bump `CACHE` in `sw.js` (e.g. `-v2`) so installed
copies pick up the update.
