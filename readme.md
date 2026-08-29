Make smaller PDFs or EPUBs out of your book files with this single page application. Useful for speed reading books on mobile.

## Useful links

- [PDF Page Extractor](https://pdf-page-extractor.pages.dev/)
- [Speed Reader](https://rsvp-reading-1.onrender.com/)
  - [(Git repo)](https://github.com/mal2994/rsvp-reading)

## Google Drive setup

1. In Google Cloud Console, create or select a project.
2. Enable the Google Picker API and Google Drive API.
3. Create an API key and an OAuth 2.0 Web application client ID.
4. Add the exact origin where this app runs to the OAuth client's authorized JavaScript origins. For local use, serve this folder over `http://localhost` or `http://localhost:8000` and add that exact origin to the OAuth client. Do not open `index.html` directly from the filesystem; Google rejects `file://` origins with `invalid_request`.
5. Set `GOOGLE_CLIENT_ID` and `GOOGLE_API_KEY` near the top of the main script in `index.html`.
6. Run a local web server from this folder, for example: `python -m http.server 8000` and then open `http://localhost:8000`.

The Drive integration requests read-only access, filters for PDF and EPUB files, and downloads the selected file locally for extraction. No Drive files are uploaded or modified.

> This project has no build step; it is a static HTML app. The Google client ID and API key are embedded in the frontend, which is normal for a browser-only app. They are restricted by allowed origins and test-user access, so they are effectively unusable to others unless they match the same origin and Gmail account. This is a pragmatic personal setup rather than a production-grade security model. Google client secret is not exposed here.
