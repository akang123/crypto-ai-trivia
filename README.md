# The Agent Economy Field Test

Public, no-login trivia game for the Merkle Research newsletter launch.

Live game: https://akang123.github.io/crypto-ai-trivia/

Repository: https://github.com/akang123/crypto-ai-trivia

## Files

- `index.html` — the full responsive game and interface.
- `assets/merkle-icon.png` — the Merkle Research logo used in the header, browser icon, and social previews.
- `questions.json` — the editable 10-question bank.
- `announcement.md` — launch copy for the newsletter or social post.
- `brand.md` — the black-and-white visual direction.

## Update the questions

Edit `questions.json`, then publish the changed file alongside `index.html`. Each question needs:

- `id` — unique slug.
- `category` — short editorial label.
- `kicker` — small section label.
- `question` — the prompt.
- `options` — exactly four answer strings.
- `answer` — zero-based index of the correct option (`0` to `3`).
- `explanation` — short explanation shown after an answer.

The game uses the first ten entries in the file for each round.

## Run locally

From this folder, run a static server so `questions.json` can load:

```bash
python3 -m http.server 4173
```

Then open `http://127.0.0.1:4173`.

## Hosting

GitHub Pages is configured from the root of the `main` branch. Push the folder contents to update the public game.
