# 言葉 Kotoba — Japanese Study App

> *継続は力なり — Persistence is power*

A fully offline-capable, installable Japanese study app built as a single HTML file. No accounts, no servers, no subscriptions — everything lives on your device.

---

## Getting Started

1. **Download** `kotoba.html`
2. **Open** it in any modern browser (Chrome, Safari, Firefox, Edge)
3. **Install** it as an app (optional — see [Installation](#installation-as-an-app))
4. Start studying

That's it. No build steps, no dependencies to install, no internet required after the first load.

---

## Features

### 📖 Scripts
| Section | What you can do |
|---|---|
| **Hiragana** | View all 46 characters, click to mark as learned, take a multiple-choice quiz |
| **Katakana** | Same as Hiragana — full chart + quiz |
| **Kanji** | Browse JLPT N5–N2 kanji, view readings & stroke count, bookmark favourites, add your own custom kanji, remove any entry |

### 🗣️ Learning Tools
| Section | What you can do |
|---|---|
| **Vocabulary** | Search & filter by JLPT level, add custom words with readings and example sentences, remove words |
| **Flashcards** | Flip cards, rate as Easy/Hard, browse by deck, add new cards, remove entire decks |
| **Writing Studio** | Draw kanji on a canvas with pen/eraser, cycle through N5 characters for stroke practice |
| **Diary** | Write daily Japanese journal entries with quick-insert buttons for common particles, save & review past entries, remove entries |

### 📚 Resources
| Section | What you can do |
|---|---|
| **PDF Library** | Upload PDF files or add Google Drive / webpage URLs as sources, open everything in the built-in in-app viewer, filter by level (A1/A2/B1/Grammar/Kanji/Reading), remove items |
| **Audio Library** | Upload audio files or add source URLs, play with speed control (0.75×–1.5×), remove items |
| **YouTube** | Paste any YouTube URL to add it to a playlist, watch in-app, take notes, remove videos |
| **Bookmarks** | Save websites with tags and notes, add Google Drive sources that open in-app, remove bookmarks |

### 🌐 Utilities
- **Quick Translator** — floating translate button (bottom-right); connect your own API for live results
- **Sakura Petals** — toggleable ambient animation
- **Search** — vocabulary search bar in the top bar

---

## Installation as an App

Kotoba is a **Progressive Web App (PWA)**. Once installed it works fully offline, opens without a browser address bar, and lives on your home screen like a native app.

### Android (Chrome)
1. Open `kotoba.html` in Chrome
2. Tap the **⋮ menu → "Add to Home Screen"**
3. Or wait 3 seconds — an install banner appears automatically

### iPhone / iPad (Safari)
1. Open `kotoba.html` in Safari
2. Tap the **Share button** (box with arrow)
3. Scroll down and tap **"Add to Home Screen"**

### Desktop (Chrome / Edge)
1. Open `kotoba.html` in Chrome or Edge
2. Look for the **install icon** in the address bar (right side)
3. Click it and confirm — or go to **Settings → Install Kotoba**

### Settings Page Shortcut
Inside the app: **Settings → Install App** has a one-tap Install button and platform-specific instructions.

---

## Data & Privacy

- **All data is stored locally** in your browser's `localStorage` — nothing is sent anywhere
- Works **fully offline** after first load (service worker caches the app)
- **Export** your data any time: Settings → Data Management → Export (downloads a `.json` backup)
- **Import** a backup: Settings → Data Management → Import
- **Clear all data**: Settings → Data Management → Clear

### Storage keys used
All keys are prefixed with `kotoba_` so they don't conflict with other apps:
`kotoba_hira`, `kotoba_kata`, `kotoba_kbm`, `kotoba_vocab`, `kotoba_fc`, `kotoba_diary`, `kotoba_pdfs`, `kotoba_audio`, `kotoba_yt`, `kotoba_ytnotes`, `kotoba_bm`

---

## Adding Sources (Google Drive / Web Pages)

PDF Library, Audio Library, and Bookmarks all have an **"Add Source"** button that accepts any URL:

- **Google Drive files** — paste a share link (`drive.google.com/file/d/...`). The app automatically converts it to an embeddable preview.
- **Google Docs** — paste the doc URL; it opens in preview mode inside the app.
- **Any webpage** — paste any `https://` URL to open it in the built-in viewer.

> **Tip:** For Google Drive files, make sure sharing is set to *"Anyone with the link can view"* so the embed loads correctly.

---

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `Space` | Flip the current flashcard |
| `→` | Next flashcard |
| `←` | Previous flashcard |
| `Escape` | Close the in-app viewer |

---

## Customisation (Settings)

| Option | Description |
|---|---|
| Sakura Petals | Toggle the falling petal animation |
| Font Size | Small / Medium / Large |
| Japanese Font | Noto Serif JP or Shippori Mincho |
| Auto-advance | Move to next flashcard automatically after rating |
| Show romanization | Toggle romaji display on flashcards |
| Shuffle deck | Randomise flashcard order |

---

## Technical Notes

- **Single file** — the entire app is one `.html` file with no external dependencies except Google Fonts (loaded on first use; cached for offline)
- **No framework** — plain HTML, CSS, and vanilla JavaScript
- **PWA** — includes a web app manifest and service worker for offline support and home screen installation
- **Responsive** — mobile-first layout with a bottom navigation bar on small screens and a sidebar on desktop; safe-area insets for iPhone notch/home bar support
- **~2200 lines** of self-contained code

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 80+ | ✅ Full (including PWA install) |
| Edge 80+ | ✅ Full (including PWA install) |
| Safari 14+ (iOS/macOS) | ✅ Full (Add to Home Screen for PWA) |
| Firefox 75+ | ✅ Full (no PWA install prompt) |
| Samsung Internet | ✅ Full |

---

## Roadmap / Ideas

- [ ] Connect a real translation API (DeepL, Google Translate)
- [ ] Stroke order animation for kanji
- [ ] SRS (Spaced Repetition) scheduling for flashcards
- [ ] Furigana toggle on vocabulary
- [ ] Import Anki decks
- [ ] Dark / light theme toggle

---

## License

This app is provided as-is for personal study use. Feel free to modify and share.

---

*言葉 Kotoba — 日本語学習の友*
