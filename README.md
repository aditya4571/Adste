# Aditya ADSTE

A self-contained S&T field register — staff, assets, ready reckoners, tasks and
inspection scheduling — built to run as a standalone app on your iPhone (or
any phone/desktop) once it's hosted on GitHub Pages.

## What's in this folder

- `index.html` — the entire app (one file: HTML, CSS and JavaScript).
- `manifest.json` — lets Android/Chrome treat it as an installable app.
- `icons/` — the app icon at the sizes iOS/Android expect.

## How the data works

This build stores everything **on your device**, in the browser's local
storage — no login, no server, works offline. That's what makes it free to
host on GitHub Pages and usable as a true standalone app.

If you were already using the Signal Yard version inside Claude (with your
664 staff and ~1,650 asset records), use the **Export backup** button on that
app's Home tab to download a `.json` file, then open this app and use
**Import backup** (also on the Home tab) to load it in. From then on, the two
copies are independent — each keeps its own data unless you export/import
between them again.

## Publish it on GitHub Pages (free)

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository — name it anything, e.g. `aditya-adste`. Make it
   Public (GitHub Pages on a free account requires a public repo).
3. Upload all three items in this folder (`index.html`, `manifest.json`, and
   the `icons` folder) to the root of that repository — GitHub's web
   interface has an "Add file → Upload files" button, so no command line or
   coding is needed.
4. In the repository, go to **Settings → Pages**. Under "Build and
   deployment", set Source to "Deploy from a branch", pick the `main` branch
   and `/ (root)` folder, then Save.
5. GitHub will publish it at a URL shaped like
   `https://<your-username>.github.io/aditya-adste/` — it takes a minute or
   two to go live the first time.

## Install it on your iPhone as a standalone app

1. Open that GitHub Pages link in **Safari** on your iPhone (must be Safari,
   not Chrome, for this step).
2. Tap the Share icon, then **Add to Home Screen**.
3. Name it and tap Add.

Because this file declares itself as an installable web app (the
`apple-mobile-web-app-capable` tag and `manifest.json`), opening it from that
Home Screen icon runs it full-screen, without Safari's address bar — as
close to a native app as a web page gets, and entirely free.

## Updating it later

If you want changes made to the app, edit `index.html` and upload the new
version to the same GitHub repository (it'll ask to replace the existing
file). Anyone who already added it to their Home Screen will get the new
version the next time they open it and it has internet access to check.
