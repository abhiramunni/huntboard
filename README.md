# HuntBoard — Job Hunt Command Centre

**Live:** https://abhiramunni.github.io/huntboard/

A single-file web app that keeps a whole job hunt on one board — from wishlist to
offer — with follow-up nudges, interview prep checklists, and an offer comparison
table. No backend, no signup, no account. Everything is stored in your browser's
localStorage and never leaves your device.

## What it does

- **Kanban board** — five stages: Wishlist → Applied → Interview → Offer, plus a
  Rejected bay (cards can move back any time). Move cards with the ◀ ▶ buttons or
  from the card's full file.
- **Follow-up nudges** — an application that goes 7 days without a reply shows up
  in the amber "Needs your attention" box (overdue at 14 days). One tap logs the
  follow-up and resets the clock.
- **Application file** — tap any card for the full dossier: pay range, applied
  date, next step, notes, a stage-change bar, and a timeline of everything that
  happened to that application.
- **Interview prep** — every interview-stage application gets its own 6-item
  preparation checklist; a general checklist covers you while you wait.
- **Offer comparison** — offers appear side by side with a rough monthly in-hand
  estimate (about 83% of CTC ÷ 12, before tax slabs — clearly labelled as rough;
  verify the exact figure before signing).
- **Weekly target** — set a weekly applications goal (default 3) and watch the
  progress ring fill; it resets every Monday.
- **Search & filters** — search by company, role or location; filter by location
  and work mode (on-site / hybrid / remote).
- **Copy hunt summary** — one-tap plain-text summary of the whole board, ready to
  paste anywhere.
- **Guides** — six plain-language playbooks: the 7-day follow-up, before the
  interview, reading an offer, after a rejection, salary talk, and keeping the
  hunt honest.

## Seeded with real applications

The board ships with 7 sample applications from a real Bengaluru fresher hunt
(Variabl — applied, awaiting review; Kenpath, Teal India, ti Steps, Smarter.Codes,
Beyond Cloud Consulting, Miamin Systems — wishlist), so the follow-up nudge,
weekly goal and stats work on first open. **Remove samples** in the footer deletes
only those; **Erase everything** wipes the board.

## How to use

1. Open the live link (or `index.html` locally — it works offline, apart from the
   Google Fonts).
2. Tap **+ Add application** and fill in company and role — the rest is optional.
3. Move cards as the hunt progresses; follow the nudges in the amber box.
4. When an interview lands, use the prep checklist; when an offer lands, compare
   it in the Offers section.

## Design

Warm editorial palette (ivory paper, espresso ink, bronze/amber/terracotta),
Fraunces + Inter, cinematic intro animation with tap-to-skip (quick on return
visits), a 3-step onboarding tour, Ken Burns photography, and inline SVG icons
throughout. Single self-contained `index.html` (~1.1 MB, including two embedded
AI-generated photographs).

## Tech

- Vanilla HTML/CSS/JS — no framework, no build step, no backend.
- Persistence: `localStorage` key `huntboard.v1`.
- QA: 65/65 headless jsdom assertions (`qa-test.js`), `node --check` clean, zero
  uncaught JS errors.

## Privacy

All data stays in your browser. There is no server, no analytics, and no data
sent anywhere. Clearing the site's localStorage erases the board.
