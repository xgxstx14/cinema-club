# Cinema Club

Cinema Club is a static, iPhone-friendly movie discovery and watchlist app powered by TMDB.

## Features
- Trending movies with Today and This Week options
- Popular, Streaming, On TV, For Rent, and In Theaters categories
- Movie trailer carousel with Popular and In Theaters options
- 2026 U.S. movie catalog with search, filters, sorting, and TMDB posters
- Movie details, watchlist, watched tracking, and JSON backup/import
- Responsive desktop sidebar and mobile bottom navigation
- Gold embossed emblem, deep navy/purple surfaces, and coral-orange accents

## Publish on GitHub Pages
1. Download and extract the update ZIP.
2. In your existing `xgxstx14/cinema-club` repository, replace the files in the repository root with the files from this ZIP.
3. Commit the changes to `main` and wait for GitHub Pages to finish publishing.
4. Open the website and refresh. If an older version remains, wait briefly and refresh again; the service-worker cache version was bumped for this release.

## TMDB key and saved progress
Your TMDB API key remains in browser local storage and is not included in these public files. The app keeps the same site origin and local storage keys, so existing watchlist and watched progress should remain on the same browser/device. Export a backup before replacing files as a precaution.

## Notes
This is a client-side static site. TMDB data, provider availability, and trailers depend on what TMDB currently returns for the United States. The Streaming and For Rent categories are based on TMDB watch-provider discovery data.
