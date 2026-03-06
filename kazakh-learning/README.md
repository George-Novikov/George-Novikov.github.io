# Қазақша — Advanced Drill PWA

A daily Kazakh language production drill app, designed for intermediate learners.
Built around *The Lord of the Rings* Kazakh translation (Prologue, Chapter 1).

## Files

```
index.html   — Main app (all logic, styles, and question data)
manifest.json — PWA manifest (name, icons, display mode)
sw.js         — Service worker (offline caching)
icon-192.png  — Home screen icon (192×192)
icon-512.png  — Home screen icon (512×512)
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `kazakh-drill`)
2. Push all files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/kazakh-drill.git
   git push -u origin main
   ```
3. Go to **Settings → Pages → Source** → select `main` branch, root folder
4. Your app will be live at: `https://YOUR_USERNAME.github.io/kazakh-drill/`

> **Important**: GitHub Pages serves over HTTPS, which is required for PWA service
> workers to function. This will work correctly once deployed.

## Install on Android

1. Open the URL in **Chrome** on your Android phone
2. A banner will appear: "Install app for daily use" → tap **Add to Home**
3. Or: tap Chrome menu (⋮) → **Add to Home screen**
4. The app now works **offline** after first load

## Update the app

Edit `index.html` to add new questions. After pushing to GitHub:
- Increment the cache version in `sw.js`: change `kazakh-drill-v1` → `kazakh-drill-v2`
- This forces Android to fetch the new version on next open

## Question Banks

| Mode      | Questions |
|-----------|-----------|
| Sentence  | Build full sentences from word banks |
| Suffix    | Chain 2–3 suffixes onto a root word |
| Error     | Find and correct grammatical mistakes |
| LotR      | Translate sentences from/to Prologue §1 |
| Flash     | Vocabulary flashcards from the prologue |
| Mixed     | 3 sentence + 2 suffix + 2 error + 2 LotR + 1 flash |
