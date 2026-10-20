# Cinema Club rebuild

Contains the 114 movie records recovered from the supplied watchlist HTML. Watched status starts as unwatched because that HTML did not contain saved progress. If you have an old valid JSON backup, import it after installing.

## Upload
Extract this ZIP and upload/replace the six app files at the root of your GitHub repository: `index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, and `icon.svg`. Commit to `main`, wait for GitHub Pages to publish, then test the live site.

## Backups
↥ downloads a JSON backup; ↧ imports a backup and asks before replacing the current data. Keep a copy somewhere outside the app. Browser storage can be erased, so back up regularly.

## TMDB
The striped-square button opens poster settings. The API key is stored locally in this browser, not in the public files or backup. Requests can be inspected by someone with access to the device/network. Do not commit your key to GitHub.
