# Codenames — Offline

A single-file, offline party game for playing Codenames in person with friends, using everyone's own phones. No internet connection, server, or install required.

## How to run it

Just open `index.html` in any web browser (double-click it, or drag it into a browser tab). Everything — code, styling, and word lists — is contained in that one file, so it works on a phone, tablet, or laptop with no network at all. Everyone opens the same `index.html` file on their own device.

If you'd rather host it (e.g. GitHub Pages, or a local server so it's one link to open instead of sharing a file), any static file host works — there's no backend.

## How to play

1. Split into a Red team and a Blue team. Each team picks one **Spymaster**; everyone else is a **Guesser**.
2. One phone becomes **"The Board"** — set it in the middle of the table so all the guessers can see the word grid. Whoever set it up picks one or more languages (English, Spanish, French, and/or Hindi — romanized in English letters, no Devanagari) and who goes first, then taps **Start Game**. Picking more than one language mixes words from all of them onto the same board.
3. The Board shows a short **Game Code** (like `HR-048291`). Each Spymaster opens `index.html` on their **own phone**, chooses **"A Spymaster"**, types in that code, and privately sees the color key for every word — no need to hide anything from guessers, and it works with zero internet connection because both devices deterministically rebuild the identical board from that one code.
4. The spymaster gives a one-word clue plus a number (say it aloud, or type it into the Board's clue box).
5. Guessers tap words on the Board. Your own team's color keeps your turn going; the other team's color, a neutral (tan) word, or manually tapping **End Turn** passes the turn. The black **Assassin** card ends the game instantly for whoever taps it.
6. First team to reveal all of their words wins.

Only have one phone total? The Board also has a **Reveal Key (fallback, this device)** button — spymasters huddle around it while guessers look away, then hide it again before guessing resumes.

## Notes

- The game code encodes which language(s) are in play, the starting team, and a random seed — nothing else is transmitted or stored anywhere; both devices just run the same shuffle algorithm from that seed.
- When multiple languages are selected, any word that happens to be spelled the same in more than one of them (common with loanwords, e.g. "HOTEL" or "TRAIN") only appears once on the board.
- A spymaster's key screen lets them tap a word to cross it off once it's been guessed, purely as a personal memory aid — it's local to their phone and doesn't affect the real board.
- Starting a new board always generates a fresh code, so spymasters need to re-enter it each round.
