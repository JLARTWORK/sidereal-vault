# AlbumOrg

**Dead-simple album organizer.**  
Built for Sore Heart Soar • 2026

Upload tracks, reorder them, add notes/moods/BPM/status, preview the whole thing with waveforms. 100% private, runs in your browser, no accounts, no servers. Perfect placeholder while you build the real thing.

**Live site:** https://albumorg.netlify.app

---

## Features

- ✨ Elegant cosmic UI (Space Grotesk display + Inter)
- 🎵 Upload any audio files (MP3, WAV, FLAC, OGG, M4A...)
- 🖱️ Drag-and-drop reordering powered by SortableJS
- 🌊 Per-track waveform visualization with Wavesurfer.js
- 📝 Rich per-track metadata: mood, BPM, notes, status (idea → final)
- 🖼️ Clickable album artwork (swap anytime)
- ▶️ "Play Album" full sequential preview mode with progress
- 📤 Export ordered track list as clean text
- 💾 Metadata auto-saved to localStorage (audio stays in-memory for session)
- 🌓 Dark-first design with subtle gold accents and kintsugi glow
- 📱 Fully responsive

## How It Works

1. **Upload tracks** — click the big upload area or drag files in
2. **Edit details** — click any track to open the editor (title, mood, BPM, notes, status)
3. **Reorder** — drag the grip handle on the left
4. **Play** — use the bottom global player or "Play Album" for the full experience
5. **Persist** — close the tab and come back; your track order and metadata return (re-upload audio after refresh)

> **Note:** Audio blobs are intentionally not persisted to localStorage (they would be huge). Your data survives refreshes.

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
   Choose `JLARTWORK/sidereal-vault` (the GitHub repo behind AlbumOrg)

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
3. Your site will live at `https://jlartwork.github.io/sidereal-vault/` (or just use the Netlify one)

## Local Development

Just open `index.html` in any browser. No server required.

```bash
open index.html
# or
python3 -m http.server 8000
```

## Data Portability

- **Export List** — copies the current ordered track list as a clean .txt
- **Reset** — nuclear option (clears everything)

For full backups of metadata, the data lives in `localStorage` under the key `albumorg-v1`. You can export/import via DevTools if needed.

## License

MIT — free to use, modify, and host for your own creative projects.

---

Built with intention by Sore Heart Soar.  
*Simple tool for getting the album in order.*

## Credits

- Design & code: Sore Heart Soar + Grok
- Icons: Font Awesome
- Waveforms: Wavesurfer.js
- Fonts: Inter & Space Grotesk (Google Fonts via CDN)
