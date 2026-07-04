# AuraSync Portfolio Cloud — Prank Simulation 🤡

A slick, fake "hacking in progress" website built purely for harmless pranks. It simulates a premium cloud dashboard scanning and archiving your photos/videos — then reveals it was all fake.

**100% client-side. No backend, no data collection, no real device access.**

---

## 🎬 What It Does

1. **Landing Screen** — A clean, professional-looking "AuraSync Portfolio Cloud" dashboard with a *"Grant Access & Initialize Studio"* button.
2. **Terminal Phase** — Displays fake system logs (`[SYSTEM]`, `[SECURITY]`, `[STORAGE]`, `[INDEXER]`) and randomly generated stats like *"4,821 Photos Indexed"*.
3. **Archive Phase** — An animated progress bar sweeps from 0–100% while fake filenames (`IMG_2026_07_04_001.jpg`, etc.) flash rapidly, alongside live counters for photos/videos processed, archive size, and transfer rate.
4. **Cancel Interrupt** — Tapping *"Cancel Operation"* freezes the bar and shows a glassmorphism modal with a dramatic (but harmless) countdown.
5. **The Reveal** — A funny, sarcastic "gotcha" screen confirms nothing real ever happened: *"No files were touched. No data left your phone."*
6. **Replay** — Resets the whole simulation instantly.

---

## ⚠️ Important: What This Project Does NOT Do

This is a **visual simulation only**. It never:

- Accesses device storage, photos, or the gallery
- Uploads, reads, or transmits any files
- Sends any data to a server (there is no backend at all)
- Requests unnecessary device permissions

Every number, filename, and stat shown is **randomly generated in the browser** using `Math.random()`. The only real browser API used is `navigator.userAgent` (to display a device/browser label like *"iPhone · Safari"*), and optionally `navigator.vibrate()` for haptic feedback — both are standard, non-invasive browser features.

---

## 🛠️ Tech Stack

- **HTML5** — semantic structure
- **CSS3** — glassmorphism, animations, fully responsive (mobile-first)
- **Vanilla JavaScript** — no frameworks, no libraries, no build step
- **Fonts** — [Inter](https://fonts.google.com/specimen/Inter) (UI) & [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (terminal/logs)

No npm, no bundler, no dependencies. Just open `index.html` or deploy the static files as-is.

---

## 📁 Project Structure

```
aurasync-prank/
├── index.html      # Page structure & all phase markup
├── style.css        # Theme, layout, animations
├── script.js         # Phase logic, fake data generation, timers
└── README.md        # This file
```

---

## 🚀 Getting Started

### Run Locally
1. Clone this repo:
   ```bash
   git clone https://github.com/your-username/aurasync-prank.git
   ```
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   npx serve .
   ```

### Deploy (Free & Instant)
This is a static site — deploy it anywhere for free:

- **[Netlify Drop](https://app.netlify.com/drop)** — drag & drop the folder, get a live link instantly
- **[Vercel](https://vercel.com)** — import the repo or drag-drop deploy
- **[GitHub Pages](https://pages.github.com/)** — enable Pages in repo settings, pointed at `main` / root
- **[Cloudflare Pages](https://pages.cloudflare.com)** — connect the repo and deploy

Once deployed, just share the URL — it works on any modern mobile or desktop browser.

---

## 🎨 Customization

- **Colors & fonts** — edit the CSS custom properties at the top of `style.css` (`:root` block)
- **Fake stats ranges** — adjust the `randInt()` ranges inside `script.js` (e.g. photo/video counts, storage %)
- **Timing** — tweak the `wait()` durations in each phase function to speed up or slow down the simulation
- **Reveal message** — edit the text directly inside the `#phase-final` section in `index.html`

---

## 📱 Browser Support

Works on all modern browsers (Chrome, Safari, Firefox, Edge) on both Android and iOS. Fullscreen mode and vibration feedback require HTTPS and are gracefully skipped if unsupported — the simulation still runs normally either way.

---

## 📄 License

Free to use, modify, and share for fun, non-malicious purposes.

---

## ⚡ Disclaimer

This project is intended purely as a **lighthearted prank tool** among friends who understand it's a joke. It does not damage devices, does not access personal data, and does not perform any real "hacking." Please use responsibly and only on people who will find it funny, not distressing.
