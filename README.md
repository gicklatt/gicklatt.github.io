# gicklatt.github.io

The Gicklatt studio site — a portfolio landing page and the **shared
`app-ads.txt`** that authorizes ad inventory for every Gicklatt game.

## Why this repo exists

`app-ads.txt` is **account-level**, not app-level. AdMob's crawler takes
the developer website from each store listing, reduces it to the root
domain (`gicklatt.github.io`) and fetches `/app-ads.txt`. A single file
here therefore covers every game — no per-game copy is needed.

If you ever add an ad-mediation network (AppLovin, Unity, ironSource,
Meta), add its line to `app-ads.txt` **here only**.

## Structure

- `index.html` — studio portfolio, links to each game's page
- `app-ads.txt` — shared AdMob authorization (root-level, required)
- `.nojekyll` — disables Jekyll processing

## Games (each lives in its own repo)

| Game      | Repo            | URL                                  |
|-----------|-----------------|--------------------------------------|
| ChessPawn | `chesspawngame` | gicklatt.github.io/chesspawngame     |
| Pallor    | `pallorgame`    | gicklatt.github.io/pallorgame        |

## Deploy

GitHub Pages → Settings → Pages → **Deploy from a branch** → `main` / root.
Plain static HTML, no build step.
