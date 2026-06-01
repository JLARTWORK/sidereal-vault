# Sidereal Vault

**A cosmic personal music album vault and track curator.**  
Built for Sore Heart Soar • 2026

Drag, drop, annotate, and preview your tracks in a beautiful dark interface with gold kintsugi accents. Everything runs 100% in your browser — private, offline-capable, no accounts, no servers.

**Live site:** https://sidereal-vault.netlify.app (deploying...)

---

## Features

- ✨ Elegant cosmic UI (Space Grotesk display + Inter)
- 🎵 Upload any audio files (MP3, WAV, FLAC, OGG, M4A...)
- 🖱️ Drag-and-drop reordering powered by SortableJS
- 🌊 Per-track waveform visualization with Wavesurfer.js
- 📝 Rich per-track metadata: title, mood, BPM, notes, completion %
- 🖼️ Clickable album artwork (swap anytime)
- ▶️ "Play Album" full sequential preview mode with progress
- 📤 Export ordered track list as clean text
- 💾 Metadata auto-saved to localStorage (audio stays in-memory for session)
- 🌓 Dark-first design with subtle gold accents and kintsugi glow
- 📱 Fully responsive

## How It Works

1. **Upload tracks** — click the big upload area or drag files in
2. **Edit details** — click any track to open the editor (title, mood, BPM, notes, status)
3. **Reorder** — drag the grip handle on the left of each row
4. **Play** — use the bottom global player or "Play Album" for the full experience
5. **Persist** — close the tab and come back; your track order and metadata return (re-upload audio after refresh)

> **Note:** Audio blobs are intentionally not persisted to localStorage (they would be huge). Your vault metadata survives refreshes and browser restarts.

## Tech Stack

- Single-file vanilla HTML (no build step)
- Tailwind CSS via Play CDN
- Font Awesome 6 icons
- SortableJS (drag & drop)
- Wavesurfer.js v7 (waveforms + playback)
- Pure client-side JavaScript + localStorage

## Deploying to Netlify (Recommended)

This project is optimized for instant static hosting.

### One-Click Deploy

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/JLARTWORK/sidereal-vault)

*(Button will work once repo is public and you have connected GitHub to Netlify)*

### Manual Steps (30 seconds)

1. **Connect GitHub**  
   Go to [Netlify](https://app.netlify.com) → "Add new site" → "Import an existing project" → GitHub → authorize if needed.

2. **Select this repo**  
   Choose `JLARTWORK/sidereal-vault`

3. **Configure build**  
   - Build command: *(leave empty)*
   - Publish directory: `.`  (or `/`)

4. **Deploy**  
   Netlify will instantly publish it at a beautiful `*.netlify.app` URL.

You can also connect a custom domain later in Netlify settings.

## Alternative: GitHub Pages

If you prefer GitHub Pages instead:

1. Repo Settings → Pages
2. Source: Deploy from a branch → `main` / root
3. Your site will live at `https://jlartwork.github.io/sidereal-vault/`

## Local Development

Just open `index.html` in any browser. No server required.

```bash
open index.html
# or
python3 -m http.server 8000
```

## Data Portability

- **Export List** — copies the current ordered track list (titles + artists) to clipboard as markdown-ready text
- **Reset Vault** — nuclear option (also clears localStorage)

For full backups of metadata, the data lives in `localStorage` under the key `sidereal_vault_tracks`. You can export/import via DevTools if needed.

## License

MIT — free to use, modify, and host for your own creative projects.

---

Built with intention by Sore Heart Soar.  
*Every track tells a story. This vault keeps them safe among the stars.*

## Credits

- Design & code: Sore Heart Soar + Grok
- Icons: Font Awesome
- Waveforms: Wavesurfer.js
- Fonts: Inter & Space Grotesk (Google Fonts via CDN)
