# WorkLog

Your work, your story. A privacy-first, browser-based tool for collecting and organising career notes before writing or updating your resume. Built by [Minh Tran](https://www.linkedin.com/in/minhhongtran/).

> ☕ If WorkLog helped you land an interview, [buy me a coffee](https://buymeacoffee.com/minhbuilds)!

---

## What it is

WorkLog is a single HTML file that runs entirely in your browser. It gives you a structured place to capture everything you've done across your career — performance reviews, peer feedback, Slack messages, Jira tickets, LinkedIn posts, memories — before you ever open a resume template.

The idea: most people struggle to write a resume not because they've done nothing, but because they can't remember everything they've done. WorkLog fixes that by separating the *collection* phase from the *writing* phase.

No account. No server. No data leaves your browser.

---

## Quick start

1. Download `index.html`
2. Open it in any browser (Chrome, Firefox, Safari, Edge)
3. Bookmark it — that's your app

Or host it on GitHub Pages for a permanent URL:

1. Create a new repo (e.g. `worklog`)
2. Upload `index.html`
3. Go to **Settings → Pages → Deploy from branch → main → / (root)**
4. Your app is live at `https://yourusername.github.io/worklog`

---

## Features

### Entries
The core of the app. Each entry is a raw note — no polish required. Tag it by company, year, category, and source. Mark it if it has a metric. Star it if it feels strong.

### Companies
Add every employer you've worked at with start and end years. Filter the entire app by company. All entries, reference docs, and the resume prompt generator are company-aware.

### Categories
Built-in categories cover the most common types of career work: Engineering, Product, Leadership, Data & analytics, Project delivery, and Other. Remove any you don't need and add your own.

### Sources
Track where each entry came from — From memory, Email / Slack, Perf review, Jira / tickets, LinkedIn, Docs / wiki, and more. Remove defaults and add custom sources to match your workflow.

### Reference docs
A separate space for full documents — your original job description, offer letters, performance reviews, peer feedback documents. The AI prompt actively uses these to match language and keywords from your JD when writing bullets.

### File import
Upload files directly into the app:

| Format | How it's handled |
|--------|-----------------|
| `.txt` | Read as plain text |
| `.docx` / `.doc` | Text extracted in-browser via mammoth.js |
| `.pdf` | Text extracted page by page via PDF.js |
| `.png` / `.jpg` / `.jpeg` | Text transcribed via Claude API (requires internet) |
| `.json` | Restores a previous backup |

### Generate resume prompt
Click **Generate resume prompt** from any view. WorkLog bundles your entries and reference docs into a structured prompt you copy and paste into any AI tool — Claude, ChatGPT, Gemini, or anything else. The AI detects your industry, seniority, and function automatically and writes polished, results-driven bullets calibrated to your actual career level.

### Export and import
Click **Export** to download a `.json` backup of everything — entries, docs, companies, custom categories and sources. Use **Import** to restore on another device or after clearing your browser.

### Dark mode
Toggle via the **Theme** button in the sidebar.

---

## How to use it

**1. Add your companies** — sidebar → By company → +

**2. Dump everything in** — entries from perf reviews, Slack, Jira, LinkedIn, uploaded PDFs and docs. Don't filter, just capture.

**3. Star your strongest entries** — anything significant, anything with impact.

**4. Flag entries with metrics** — check "has metric" on anything with a number, %, dollar amount, or team size.

**5. Add your original JD** — Reference docs → the AI will borrow its exact language and keywords when writing bullets.

**6. Generate resume bullets** — click Generate resume prompt, copy, paste into any AI tool.

**7. Back up regularly** — Export → save to Google Drive, iCloud, or Dropbox.

---

## Privacy

Everything runs locally in your browser. No data is sent to any server except for one optional feature: image OCR (when you upload a `.png` or `.jpg`) sends the image to the Claude API to extract text. No account, no tracking, no ads.

---

## Tech stack

A single self-contained HTML file. No build step, no dependencies to install, no framework. Libraries loaded on demand from CDN only when needed:

- [mammoth.js](https://github.com/mwilliamson/mammoth.js) — `.docx` text extraction
- [PDF.js](https://mozilla.github.io/pdf.js/) — `.pdf` text extraction
- [Claude API](https://docs.anthropic.com) — image OCR only (optional)

Fonts loaded from Google Fonts: Instrument Serif, DM Mono, Geist.

---

## License

MIT — free to use, modify, and share.

---

Built by [Minh Tran](https://www.linkedin.com/in/minhhongtran/) · [Buy me a coffee ☕](https://buymeacoffee.com/minhbuilds)
