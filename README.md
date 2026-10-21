# Cinema Club — spreadsheet movie list

This build uses the 158 movie entries from `2026_US_Movie_Release_Master_List_synopses_updated(1).xlsx` and keeps the existing Cinema Club interface and features. Movie titles, release dates, genres, synopses when supplied, release types, distributors, and synopsis/date status notes were carried over where available.

Watched progress starts at zero, as requested. Movies without a synopsis are explicitly marked as needing research. Release dates and genre labels are taken from the spreadsheet and may need cross-checking where the source status says so.

## Upload
Extract this ZIP and upload/replace the seven files at the root of your GitHub repository: `index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, `icon.svg`, and `README.md`. Commit to `main`, wait for GitHub Pages to publish, then test the live site.

## Backups
The export button downloads a JSON backup; the import button restores a backup and asks before replacing current data. Keep a copy somewhere outside the app. Browser storage can be erased, so back up regularly.

## TMDB
The striped-square button opens poster settings. The API key is stored locally in this browser, not in the public files or backup. Poster matching now searches TMDB by movie title and year because this spreadsheet does not contain IMDb IDs. Check the results visually; title-based matches may occasionally need correction. Do not commit your key to GitHub.
