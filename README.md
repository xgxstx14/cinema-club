# Cinema Club — iPhone movie watchlist

This folder contains a static Progressive Web App (PWA) built from your original 114-movie list.

## What it does
- All 114 movies are included in their original order.
- Separate All Films, Watchlist, and Watched views.
- Search title, year, genre, director, and synopsis.
- Reactive genre, year, and minimum IMDb rating filters.
- Sort by original list order, title, year, rating, or unwatched first.
- Movie detail view with synopsis, director, release date, runtime, rating, genres, and IMDb link.
- Watched state and selected view are saved in browser local storage.
- Export/import a JSON backup of watched progress.
- PWA manifest, app icons, and a service worker for offline app-shell use after first load.

## Important notes
- Host it over HTTPS; opening `index.html` directly from Files is not the intended app experience. Service workers and installable PWA behavior require a secure hosted origin (localhost is the development exception).
- Watched status is saved in the browser on the device. Use **Back up progress** if you want to preserve or transfer it. Clearing Safari website data can erase local progress.
- This version does not sync progress between devices or use a remote database.
- The poster art is generated typographic artwork, not official film posters. IMDb links open the external film page.
- No user data is sent to a server by this app. The optional Google Fonts stylesheet is a third-party request; system fonts are used as fallbacks.

## Host on GitHub Pages (free)
1. Sign in to GitHub and create a new repository (for example `cinema-club-watchlist`). A public repository is easiest for a personal Pages site; assume the source files and published site will be public.
2. Upload **all files in this folder** to the top level of that repository. Make sure `index.html` is at the top level.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then Save.
5. Wait for deployment, then use the URL shown in the Pages section (usually `https://YOUR-USERNAME.github.io/cinema-club-watchlist/`).
6. Open that URL in Safari on your iPhone.
7. In Safari, tap **Share** → **Add to Home Screen**. If shown, enable **Open as Web App**, then tap **Add**.
8. Launch it from the new Home Screen icon.

## If you update files
Upload/replace the files in the repository. Refresh the site after GitHub Pages redeploys. The service worker may keep the previous version briefly; fully close and reopen the Home Screen app if it doesn't update.

## Quick local preview
You can preview it on a computer using a local web server, but opening the HTML file directly may not enable the install/offline features.


## Loading real TMDB posters

After uploading these updated files to the existing GitHub repository and waiting for Pages to publish:

1. Open `https://xgxstx14.github.io/cinema-club/`.
2. Click the small poster/settings icon near the top-right.
3. Paste your TMDB **API Key** (the shorter key, not the API Read Access Token).
4. Click **Load posters** and keep the page open while the 114 IMDb IDs are checked.
5. The matched poster paths are saved locally in that browser. Movies without a TMDB match or poster will keep the Cinema Club typographic fallback.

The API key is saved in that browser's local storage and is not included in the repository files. However, because this is a client-side public website, the key is used in browser API requests and should not be considered secret. For a personal project this may be acceptable; do not use a credential that must remain confidential. If you open the app on another device/browser, configure the key there too. Your watched state remains separate per device/browser unless you export/import your backup.

TMDB attribution: This product uses the TMDB API but is not endorsed or certified by TMDB. Movie data and poster images are provided by TMDB.


## Updates in this build
- Genre and release-year filter menus are populated directly from the full movie data and show how many options are available.
- Added an **Oldest year** sort option (ascending release year; films without a year appear last).
- Updated the service-worker cache version so installed copies refresh to the new files.
