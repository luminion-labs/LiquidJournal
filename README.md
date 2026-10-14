# LiquidJournal

A responsive, premium-feeling journal web app inspired by the supplied Liquid Glass UI reference.

## Features
- Responsive desktop, tablet and mobile layouts
- Liquid-glass cards, soft shadows, iridescent gradients and rounded controls
- Home overview, all entries, favorites, calendar, writing prompts and personalization
- Journal editor with title, date, mood, tags, lightweight Markdown-style formatting, word count and autosave
- Search, sort and tag filtering
- Multiple themes: Liquid Glass, Cloud, Obsidian, Lavender, Midnight, Rosewater and Monochrome
- Font choices: DM Sans, Manrope, Playfair Display and JetBrains Mono
- Export full JSON backup, export Markdown, export a single entry as text, and import a JSON backup
- Local browser storage; no account or backend required
- Keyboard shortcuts: Ctrl/Cmd+Enter saves; Ctrl/Cmd+K opens search

## Run locally
Open `index.html` in a modern browser. Google Fonts require internet access; system fallbacks are included.

## Deploy for free
### GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html` and this README.
3. In repository Settings → Pages, deploy from the `main` branch and `/ (root)`.
4. Open the generated Pages URL.

### Netlify / Vercel
Create a new static site and deploy the folder. No build command or output directory is required; the root contains `index.html`.

## Important privacy note
Entries are saved in `localStorage` on the current browser/device. They are not encrypted, synced between devices, or backed up automatically. Do not use a shared device for sensitive entries. Use **Personalize → Export all entries** to create a backup before clearing browser data.

## Suggested next production upgrade
If you want user accounts and secure cross-device sync, add an authenticated backend (for example Supabase) with row-level security, explicit data deletion, and a privacy policy. Do not present local storage as cloud sync.

## Install as an app (PWA)
This project now includes a web app manifest, install button, app icons, and a service worker for offline app-shell access.
1. Deploy the full `LiquidJournal` folder to a secure HTTPS host (Vercel or GitHub Pages).
2. Open the deployed site in Chrome on Android. Use the **Install** button in the header or the browser menu → **Install app** / **Add to Home screen**.
3. On iPhone/iPad, open the site in Safari → Share → **Add to Home Screen**.
4. Launch LiquidJournal from the new home-screen icon. The app shell can open offline after the first successful load; Google Fonts need an internet connection unless already cached by the browser.

PWA note: service-worker registration requires HTTPS (localhost is also supported for local development). Journal entries still live in that browser's local storage; installing the app does not add cloud sync or encryption.
