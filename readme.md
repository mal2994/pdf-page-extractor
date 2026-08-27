Make smaller PDFs or EPUBs out of your book files with this single page application. Useful for speed reading books on mobile.

The extractor also accepts EPUB files. For EPUBs, the range selects chapters in the book's reading order and downloads a new EPUB containing only those chapters.

## Google Drive setup

1. In Google Cloud Console, create or select a project.
2. Enable the Google Picker API and Google Drive API.
3. Create an API key and an OAuth 2.0 Web application client ID.
4. Add the URL where this app runs to the OAuth client's authorized JavaScript origins. For local use, serve this folder over `http://localhost` rather than opening `index.html` directly.
5. Set `GOOGLE_CLIENT_ID` and `GOOGLE_API_KEY` near the top of the main script in `index.html`.

The Drive integration requests read-only access, filters for PDF and EPUB files, and downloads the selected file locally for extraction. No Drive files are uploaded or modified.

- [PDF Page Extractor](https://pdf-page-extractor.pages.dev/)
- [Speed Reader](https://rsvp-reading-1.onrender.com/)
  - [(Git repo)](https://github.com/mal2994/rsvp-reading)
