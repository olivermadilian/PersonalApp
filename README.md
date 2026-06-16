# Liftr — Workout Tracker

A mobile-friendly workout tracker with an AI coach, built as a single HTML file.
Log your lifts, see your history, and get next-session suggestions for movements,
weights, and reps from **Claude Sonnet 4.6**.

## Use it

**Live: https://olivermadilian.github.io/PersonalApp/**

Or open `index.html` in any modern browser — phone or desktop. No build step,
no server, no install. Your data is saved in the browser (localStorage) and
stays on your device.

Every push to the development branch is mirrored to `gh-pages` by a GitHub
Actions workflow, which updates the live site automatically.

## Features

- **Log** — quick add of movement, weight, reps, and sets; live session volume,
  set, and rep totals; tap to remove an entry
- **History** — past sessions grouped by day with per-session volume
- **AI Coach** — Claude Sonnet 4.6 reviews your recent training and suggests a
  next session (movements, sets, reps, working weights) with a one-line rationale
  for each; add any suggestion — or the whole session — to today with one tap
- **Units** — switch between lb and kg (used for logging and suggestions)
- **Your data** — export/import a JSON backup, or clear everything

## AI Coach setup

The coach calls the Anthropic API directly from your browser, so it needs your
own API key:

1. Get a key at [console.anthropic.com](https://console.anthropic.com/settings/keys)
2. Open **Settings → AI Coach** and paste it in

The key is stored **only** in your browser's localStorage and is sent directly
to Anthropic when you request suggestions — it never touches any other server.
Because the key lives in the browser, use the coach on your own device only
(don't enter your key on a shared computer).

## Apple Health

A web page can't read or write Apple Health directly — that's restricted to
native iOS apps. The data model here is kept clean and exportable so workouts
can be brought into Health later via the Shortcuts app. Native sync isn't
included yet.
