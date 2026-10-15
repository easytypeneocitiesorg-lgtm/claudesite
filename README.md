# Umbra Arcade

A purple-and-black portal for open-source browser games. It hosts no games itself: each one loads in a sandboxed iframe from its own GitHub Pages site.

Plain HTML/CSS/JS in a single `index.html`. No build step, no backend, no dependencies.

## Features
Search (`/` to focus), category filters, sorting, favorites, recently played, settings, pointer-reactive background (respects reduced motion), fullscreen player.

## Run locally
    npx serve .
or open `index.html` in a browser.

## Deploy to Vercel
1. Push this folder to a GitHub repo.
2. On vercel.com choose Add New > Project, import the repo.
3. Framework Preset: **Other**. Leave build command and output directory empty. Deploy.

## Games
All entries come from the "Play it now!" links in https://github.com/leereilly/games.
Edit the `G` array near the top of the script in `index.html` to add or remove games.
Only `https://*.github.io/` URLs pass the `OK` check in the player; widen that regex if you add other hosts.

Embedding status: every game is **URL found, embedding unverified**. Test each one after deploying and replace any that refuse to load (the site shows a fallback link to the original).
