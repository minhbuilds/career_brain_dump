# Career Brain Dump

A private, browser-based tool for collecting and organizing your career history before writing or updating your resume. Built by [Minh Tran](https://github.com/minhtran).

---

## What it is

Career Brain Dump is a single HTML file that runs entirely in your browser. It gives you a structured place to capture everything you've done across your career — performance reviews, peer feedback, Slack messages, Jira tickets, LinkedIn posts, memories — before you ever open a resume template.

The idea: most people struggle to write a resume not because they've done nothing, but because they can't remember everything they've done. This app fixes that by separating the *collection* phase from the *writing* phase.

No account. No server. No data leaves your browser.

---

## Quick start

1. Download `index.html`
2. Open it in any browser (Chrome, Firefox, Safari, Edge)
3. Bookmark it — that's your app

Or host it on GitHub Pages for a permanent URL:

1. Create a new repo (e.g. `career-brain-dump`)
2. Upload `index.html` — rename it `index.html` if needed
3. Go to **Settings → Pages → Deploy from branch → main → / (root)**
4. Your app is live at `https://yourusername.github.io/career-brain-dump`

---

## Features

### Entries
The core of the app. Each entry is a raw note — no polish required. Tag it by company, year, category, and source. Mark it if it has a metric. Star it if it feels strong.

### Companies
Add every employer you've worked at with start and end years. Filter the entire app by company. All entries, reference docs, and the resume prompt generator are company-aware.

### Categories
Built-in categories cover the most common types of career work: Programs led, Platform / infra, AI / product, Wins, Feedback / reviews, Process / ops, People / leadership, and Other. You can add your own custom categories to match how you think about your work.

### Sources
Track where each entry came from — From memory, Email / Slack, Perf review, Jira / tickets, LinkedIn, Docs / wiki, and more. Add custom sources to match your workflow. Useful when you want to make sure you've mined every channel.

### Reference docs
A separate space for full documents — your original job description, offer letters, performance reviews, peer feedback documents, brag docs. These are kept distinct from entries so you can paste in long-form content without cluttering your note stream.

### File import
Upload files directly into the app:

| Format | How it's handled |
|--------|-----------------|
| `.txt` | Read as plain text |
| `.docx` / `.doc` | Text extracted in-browser via mammoth.js |
| `.pdf` | Text extracted page by page via PDF.js |
| `.png` / `.jpg` / `.jpeg` / `.gif` / `.webp` | Text transcribed via Claude API (requires internet) |
| `.json` | Restores a previous backup |

### Generate resume prompt
The key output feature. When you're ready, navigate to a company in the sidebar and click **Generate resume prompt**. The app bundles:

- All your entries for that company (or starred-only, your choice)
- Your reference docs as context
- A pre-written prompt in XYZ format

Copy it and paste it into any AI tool — Claude, ChatGPT, Gemini, or anything else. The prompt instructs the AI to turn your raw notes into polished resume bullets, flag entries missing metrics, and suggest what numbers you could look up.

You can also download the prompt as a `.txt` file to save or share.

### Export and import
Click **Export** to download a `.json` backup of everything — entries, docs, companies, and custom categories and sources. Use **Import** (via Upload file) to restore from that backup on another device or after clearing your browser cache.

### Dark mode
Toggle between light and dark theme using the **Theme** button in the sidebar header.

---

## How to use it (the full workflow)

**1. Add your companies**
Start in the sidebar under By company. Add every employer with a start and end year.

**2. Dump everything in — don't filter**
Add entries from every digital trail you can find. Use Upload file to bring in PDFs, Word docs, or screenshots. Don't worry about writing quality — raw is fine. Tag each entry but don't agonize over it.

**3. Star your strongest entries**
Once you have a solid pile, go through and star anything significant. A project that moved a number. Something leadership noticed. A time you grew beyond your role.

**4. Flag entries with metrics**
Check "has metric" on any entry that contains a number, percentage, dollar amount, or team size. These become your highest-value resume bullets.

**5. Add your original job description**
Go to Reference docs and add the JD you were hired for. This helps the AI understand your scope and match the language your employer used — which often lines up with what future employers search for.

**6. Generate resume bullets**
Navigate to a company in the sidebar. Click **Generate resume prompt** in the top right. Copy the output and paste it into Claude, ChatGPT, or any AI. You'll get polished XYZ-format bullets back, with flags on anything that's missing a metric.

**7. Back up regularly**
Click **Export** and save the file to Google Drive, iCloud, or Dropbox. Your data lives in browser localStorage — it won't survive a browser reset or device switch without a backup.

---

## Privacy

Everything runs locally in your browser. No data is sent to any server except for one optional feature: image OCR (when you upload a `.png` or `.jpg`) sends the image to the Claude API to extract text. All other file types are processed entirely offline. No account, no tracking, no ads.

---

## Tech stack

A single self-contained HTML file. No build step, no dependencies to install, no framework. Libraries are loaded on demand from CDN only when needed:

- [mammoth.js](https://github.com/mwilliamson/mammoth.js) — `.docx` text extraction
- [PDF.js](https://mozilla.github.io/pdf.js/) — `.pdf` text extraction
- [Claude API](https://docs.anthropic.com) — image OCR only (optional)

Fonts loaded from Google Fonts: Instrument Serif, DM Mono, Geist.

---

## License

MIT — free to use, modify, and share.

---

Built by Minh Tran
