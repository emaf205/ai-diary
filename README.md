# AI Diary

A public, minimal diary of what I build, test, discover and question while working with AI.

**Live:** https://emaf205.com/ideas/ai-library

![AI Diary interface](assets/screenshot.jpg)

## The project

AI Diary started from a simple problem: important experiments, discoveries, ideas and decisions were disappearing inside long ChatGPT conversations.

Instead of writing a traditional blog post for every small discovery, I turned the conversation history into a chronological micro-journal. Each entry is written in the first person, stays within 140 characters, varies naturally in length and can include hashtags, public links, screenshots and occasional dilemmas.

The result is not a transcript archive. It is a compressed public history of my work with AI.

## What enters the diary

- things I build;
- AI experiments;
- discoveries;
- prompts and workflows;
- lessons and teaching experiments;
- prototypes and small tools;
- published projects;
- failures and unexpected results;
- ideas worth keeping;
- occasional open questions or dilemmas.

Empty days stay empty. No filler is added just to make the timeline look complete.

## Privacy by design

Before publication:

- client and company names are anonymized;
- personal names are removed when unnecessary;
- email addresses and identifying data are excluded;
- sensitive or confidential material is never published;
- dates, links and claims are never invented.

The repository intentionally does **not** contain a separate historical Markdown archive of all posts.

## Interface

AI Diary is a static, responsive web app with:

- weekly blocks;
- full-text search;
- clickable hashtags;
- period filters and custom date range;
- light / dark mode;
- public project links;
- optional real screenshots;
- mobile-first single-column layout.

No framework, database or backend is required.

## PWA: install it like an app

AI Diary is also a Progressive Web App.

On supported Android browsers and desktop browsers an **Installa** action appears automatically. On iPhone/iPad, open the site in Safari and use:

**Condividi → Aggiungi alla schermata Home**

The PWA includes:

- a custom AI Diary app icon in PNG + scalable SVG;
- standalone app mode;
- mobile home-screen installation;
- local cache for the interface;
- offline fallback for already cached pages/assets;
- saved light/dark preference.

### App icon

The icon was designed specifically for this project: an open diary with a small light/spark above it, using the blue/violet visual language of the interface.

## Automated update workflow

AI Diary is not maintained only by hand.

A scheduled ChatGPT task runs **every 3 days** and reviews the recent work available in my conversations.

The automation:

1. finds new AI-related activities, experiments, discoveries, ideas and dilemmas;
2. removes duplicates and low-value filler;
3. rewrites useful events as first-person micro-posts of no more than 140 characters;
4. deliberately keeps posts at different lengths;
5. adds one to three relevant hashtags;
6. adds verified public links when available;
7. anonymizes companies, clients, people and sensitive data;
8. includes real screenshots only when available, relevant and safe to publish;
9. preserves weekly grouping, search, filters, PWA and theme toggle;
10. updates the project version of `index.html`;
11. produces a fresh HTML version ready for FTP deployment.

The live site is deployed manually via FTP. The automation prepares the update; I keep the final publication step under my control.

## Why

I wanted something between a changelog, a lab notebook, a personal research timeline, early Twitter and a public memory of working with AI.

The interesting part is not only what gets finished. The diary also preserves small discoveries, failed attempts and doubts that would normally disappear inside chats.

## Project structure

```text
.
├── index.html
├── manifest.webmanifest
├── sw.js
├── assets/
│   ├── icon.svg
│   ├── icon-180.png
│   ├── icon-192.png
│   └── screenshot.jpg
├── LICENSE
└── README.md
```

## Run locally

For a simple preview, open `index.html`.

For full PWA/service-worker behaviour, serve the folder through HTTP/HTTPS. The production version runs at:

https://emaf205.com/ideas/ai-library

## Author

**Emanuele BDC**

- Homepage: https://emaf205.com/
- Blog: https://emaf205.com/blog/
- Ideas: https://emaf205.com/ideas/
- GitHub: https://github.com/emaf205

---

An experiment in turning everyday AI conversations into a living public research diary.
