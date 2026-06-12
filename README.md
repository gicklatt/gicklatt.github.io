# gicklatt.github.io

The **Gicklatt studio site** — a portfolio landing page and the shared
`app-ads.txt` that authorizes ad inventory for every Gicklatt game.

🔗 **Live:** [gicklatt.github.io](https://gicklatt.github.io)

## Why this repo exists

Two jobs:

1. **Studio portfolio** — a premium landing page showcasing every game.
2. **Shared `app-ads.txt`** — AdMob authorization for all ad-supported games.

`app-ads.txt` is **account-level**, not app-level. AdMob's crawler takes
the developer website from each store listing, reduces it to the root
domain (`gicklatt.github.io`) and fetches `/app-ads.txt`. A single file
here therefore covers every game — no per-game copy is needed.

> If you ever add an ad-mediation network (AppLovin, Unity, ironSource,
> Meta), add its line to `app-ads.txt` **here only**.

## Tech stack

- Plain static **HTML + CSS** — no build step
- Fonts: Fraunces + Inter (Google Fonts)
- Hosted on **GitHub Pages**

## Structure

| Path | Purpose |
|------|---------|
| `index.html` | Studio portfolio |
| `app-ads.txt` | Shared AdMob authorization (root-level, required) |
| `404.html` | Custom not-found page |
| `*-icon.*`, `*-shot.*` | Game artwork used on the portfolio |
| `.nojekyll` | Disables Jekyll processing |

## Games (each lives in its own repo)

| Game          | Repo                | URL                                  |
|---------------|---------------------|--------------------------------------|
| ChessPawn     | `chesspawngame`     | gicklatt.github.io/chesspawngame     |
| Color Luggage | `colorluggagegame`  | gicklatt.github.io/colorluggagegame  |
| Exhomorph     | `exhomorphgame`     | gicklatt.github.io/exhomorphgame     |
| Gambitile     | `gambitilegame`     | gicklatt.github.io/gambitilegame     |
| Pallor        | `pallorgame`        | gicklatt.github.io/pallorgame        |
| Tixxle        | `tixxlegame`        | gicklatt.github.io/tixxlegame        |

Each game is a separate **project page** repo — the URL sub-path comes
from the repository name.

## Develop

Open `index.html` in a browser, or serve locally:

```bash
python3 -m http.server 8000   # http://localhost:8000
```

## Deploy

GitHub Pages → **Settings → Pages → Deploy from a branch → `main` / root**.

---

© Gicklatt · [gicklatt@gmail.com](mailto:gicklatt@gmail.com)
