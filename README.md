# The Horror 288

A checklist of Letterboxd's top 288 horror films. Check off what you've seen, see which tier you land in, and export a share image of your score.

## Features

- All 288 posters with title, year and rank
- Click a poster or its checkbox to mark it seen. Progress saves in your browser (localStorage).
- Search by title or year, and filter by All / Seen / Not seen
- Tiers based on how many you've seen:

  | Seen | Tier |
  |---|---|
  | 0+ | 🙈 Scaredy Cat |
  | 10+ | 💡 Lights-On Sleeper |
  | 50+ | 🍿 Popcorn Screamer |
  | 100+ | 🔪 Final Girl |
  | 150+ | 🌙 Midnight Maniac |
  | 200+ | 🩸 Gorehound |
  | 250+ | 👻 Scream Fiend |
  | 288 | 👑 Horror Royalty |

- **Share my score** makes a PNG card with your count, your tier and a poster grid (seen posters lit up, the rest dimmed). You can add a name to the card.

## Project structure

```
index.html   the whole app (HTML, CSS and JS in one file)
posters/     288 poster images, 000.jpg to 287.jpg, in list order
README.md
```

No build step or dependencies. Fonts come from Google Fonts.

## Run locally

Open `index.html` in a browser. If you want the share image to work, serve the folder instead, because browsers block canvas exports from `file://`:

```
python3 -m http.server
```

Then go to http://localhost:8000.

## Deploy

Push to GitHub and import the repo in Vercel. Use the **Other** framework preset and leave the build settings empty. Every push to `main` redeploys.

## Notes

- Posters were cropped from screenshots of the Letterboxd list. Titles and years were filled in by hand, so a few could be off.
- Each browser keeps its own progress, so checkmarks don't sync between devices.
