# Cinema Club — TMDB-powered 2026 catalog

This build keeps the Cinema Club design and adds a TMDB-powered home screen:
1. What's Trending (Today / This week)
2. What's Popular with Popular, Streaming, On TV, For Rent, and In Theaters categories (plus All popular / 2026 only scope)
3. A Movie Trailers carousel with Popular and In Theaters options
4. The 2026 U.S. movie catalog with search, genre, year, release-type filters, sorting, details, watched status, and watchlist controls.

## TMDB setup
1. Publish the seven files in this ZIP to the root of your `main` branch on GitHub.
2. Open Cinema Club and tap the striped-square settings button.
3. Enter your TMDB API key (the short API key, not the long API Read Access Token) and save it.
4. Use **Load 2026 catalog and movie posters** to fetch the catalog. The catalog can take a little while because TMDB's release categories are queried separately.
5. If a TMDB key is already saved in this browser, the app loads cached data first and refreshes stale data on startup. The app caches the catalog, discovery categories, and trailer rail locally and refreshes them about once every 24 hours when online. Streaming and rental filters use TMDB U.S. watch-provider availability where TMDB has data; On TV displays popular TV shows, and In Theaters uses TMDB’s now-playing list. Trailer links open YouTube in a new tab when TMDB has a YouTube trailer available. Use **Refresh catalog** to request a manual refresh.

TMDB API calls are made from the browser, so the API key is not secret from someone who can inspect requests on that device. It is not written into these public files or included in backups.

## Catalog coverage note
TMDB is the discovery source, not a guarantee that every U.S. release is listed. Dates, release categories, genres, and synopsis availability depend on TMDB's data. The app paginates through the TMDB results for each release category, up to TMDB’s 500-page API limit per category. Categories can overlap; duplicate movie IDs are merged. The existing spreadsheet list remains as a fallback if TMDB has not been configured.

## Watchlist and backups
Use **＋ Watchlist** on a carousel card, catalog card, or movie detail screen. Watchlist membership is separate from watched status and persists on this device. Export a JSON backup regularly; browser storage can be cleared by the browser or device.
