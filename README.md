# AI Diary

A public, minimal diary of what I build, test, discover and question while working with AI.

**Live version:** https://emaf205.com/ideas/ai-library

![AI Diary interface](assets/screenshot.png)

## The project

AI Diary started from a simple problem: important experiments, discoveries, ideas and decisions were disappearing inside long ChatGPT conversations.

Instead of writing a traditional blog post for every small discovery, I turned the conversation history into a chronological micro-journal.

Each entry behaves like an early Twitter post:

- maximum 140 characters;
- first person;
- intentionally variable length;
- date and time when available;
- one to three topic hashtags;
- a public link when the project or resource is online;
- occasional dilemmas when the doubt itself is part of the work.

The result is not a transcript archive. It is a compressed public history of my work with AI.

## What goes into the diary

The feed can include:

- things I built;
- AI experiments;
- discoveries;
- prompts and workflows;
- lessons and teaching experiments;
- prototypes and small tools;
- published projects;
- failures and unexpected results;
- ideas worth keeping;
- occasional open questions or dilemmas.

Only entries that add something useful to the timeline are kept. Empty days stay empty.

## Privacy by design

The public diary is intentionally filtered.

Before publication:

- client and company names are anonymized;
- personal names are removed when unnecessary;
- email addresses and identifying information are excluded;
- sensitive or confidential material is never published;
- unverifiable dates, links and claims are not invented.

The repository does **not** contain a separate historical Markdown archive of all posts.

## Interface

The site is a standalone static HTML application.

It includes:

- weekly blocks;
- full-text search;
- clickable hashtags;
- filters by period;
- custom date range;
- light / dark mode;
- public project links;
- responsive mobile layout.

No framework, database or backend is required.

## Automated update workflow

AI Diary is not maintained only by hand.

A scheduled ChatGPT task runs **every 3 days** and reviews the recent work available in my conversations.

The automation:

1. finds new AI-related activities, experiments, discoveries, ideas and dilemmas;
2. removes duplicates and low-value filler;
3. rewrites useful events as first-person micro-posts of no more than 140 characters;
4. adds relevant hashtags;
5. adds verified public links when available;
6. anonymizes companies, clients, people and sensitive data;
7. includes real screenshots only when they are available, relevant and safe to publish;
8. preserves the weekly feed structure, search, filters and theme toggle;
9. updates the project version of `index.html`;
10. produces a fresh HTML file ready to upload to my FTP space.

The live site is intentionally deployed manually via FTP. The automation prepares and updates the feed; I keep the final publication step under my control.

## Why

I wanted something between:

- a changelog;
- a lab notebook;
- a personal research timeline;
- early Twitter;
- and a public memory of working with AI.

The interesting part is not only what was finished. The diary also preserves small discoveries and occasional doubts that would normally disappear inside chats.

## Project structure

```text
.
├── index.html
├── assets/
│   └── screenshot.png
├── LICENSE
└── README.md
```

## Run locally

No installation is required.

Download the repository and open:

```
index.html
```

in any modern browser.

It can also be uploaded directly to a normal FTP/static web space.

## Live

**AI Diary**  
https://emaf205.com/ideas/ai-library

## Author

**Emanuele BDC**

- Homepage: https://emaf205.com/
- Blog: https://emaf205.com/blog/
- Ideas: https://emaf205.com/ideas/
- GitHub: https://github.com/emaf205

---

An experiment in turning everyday AI conversations into a living public research diary.
