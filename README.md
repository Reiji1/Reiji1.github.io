# Jammming

Jammming is a React-powered Spotify playlist builder. Search the Spotify catalog, assemble a custom playlist, and export it straight to your account using Spotify's Web API.

## Purpose

This project was built to practice React component patterns, state management, and third-party API integration while delivering a fully client-side playlist experience that works on GitHub Pages.

## Technologies

- React via CDN (no build tooling required)
- Spotify Web API
- Modern CSS with custom properties
- GitHub Pages-friendly static hosting

## Features

- Search Spotify for tracks by song title, artist, or album
- View track details (title, artists, album) for search results
- Build a custom playlist by adding/removing tracks
- Name your playlist and export it directly to your Spotify account
- Lightweight client-only OAuth flow (implicit grant) with saved tokens in `localStorage`

## Getting Started

1. **Create a Spotify app** at [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard) and note your Client ID.
2. **Add a redirect URI** to your Spotify app that matches your deployment URL (e.g., `https://<username>.github.io/` or your local file URL for testing).
3. **Open `index.html`** locally or via GitHub Pages.
4. **Paste your Client ID** into the "Connect to Spotify" panel and click **Authorize**. Approve the requested scopes to return with an access token stored in your browser.
5. **Search for songs**, add them to your playlist, choose a playlist name, and click **Save to Spotify**.

### Environment notes

- The app uses the implicit grant OAuth flow entirely in the browser. No secrets are stored or transmitted to any server.
- Tokens and Client IDs are cached in `localStorage`; clear your storage to reset.
- If you receive authorization errors, re-run the authorization flow to refresh your token.

## Future Work

- Add audio previews and album art to results
- Support reordering tracks via drag-and-drop
- Persist multiple playlists locally for quick reuse
- Add validation for duplicate playlist names and better error messaging

## Deployment

This repository is ready for static hosting. Push to GitHub Pages or any static host; all dependencies are loaded from CDNs.
