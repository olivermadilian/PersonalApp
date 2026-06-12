# Blackjack 3D

A mobile-friendly blackjack game with 3D graphics, built as a single HTML file.

## Play it

**Live: https://olivermadilian.github.io/PersonalApp/**

Or open `index.html` in any modern browser — phone or desktop. No build step,
no server, no install. (It loads Three.js from a CDN, so it needs an internet
connection.)

Every push to the development branch is mirrored to `gh-pages` by a GitHub
Actions workflow, which updates the live site automatically.

## Features

- 3D casino table rendered with Three.js: felt with painted markings, wooden
  rim, animated card dealing and flipping, and chip stacks for your bet
- Touch-friendly UI: chip buttons for betting, Hit / Stand / Double actions
- Standard rules: dealer stands on 17, blackjack pays 3:2, double down on
  your first two cards
- Your balance is saved between sessions (and topped back up to $500 if you
  go broke)
