# Codenames — Offline

A single-file, offline party game for playing Codenames in person with friends. No internet connection, server, or install required.

## How to run it

Just open `index.html` in any web browser (double-click it, or drag it into a browser tab). Everything — code, styling, and word lists — is contained in that one file, so it works from a phone, tablet, or laptop with no network at all.

If you'd rather host it (e.g. GitHub Pages, or a local server so multiple devices on the same Wi-Fi can each open it), any static file host works — there's no backend.

## How to play

1. Gather everyone around one shared screen (a tablet or laptop works well).
2. Split into a Red team and a Blue team. Each team picks one **Spymaster**; everyone else is a **Guesser**.
3. Pick a language (English, Spanish, French, or Hindi — romanized in English letters, no Devanagari) and who goes first, then tap **Start Game**.
4. At the start of a turn, both spymasters look at the screen and tap **Reveal Key (Spymasters Only)** — guessers should look away. Tap **Hide Key** before guessers look back.
5. The spymaster gives a one-word clue plus a number (type it into the clue box, or just say it aloud).
6. Guessers tap words on the board. Your own team's color keeps your turn going; the other team's color, a neutral (tan) word, or ending manually with **End Turn** passes the turn. The black **Assassin** card ends the game instantly for whoever taps it.
7. First team to reveal all of their words wins.

## Notes

- Word usage is tracked per language in the browser's local storage so repeat boards feel fresher across games on the same device; it resets automatically once the word pool for a language is exhausted.
- Since it's a single shared screen, anyone looking at the board during "Reveal Key" mode can see the answers — that's just an inherent limit of a single-device pass-and-play design.
