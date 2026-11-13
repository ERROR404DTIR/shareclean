# ShareClean

<p align="center"><img src="assets/readme-banner.svg" alt="ShareClean animated banner" width="100%"></p>

A privacy-first image metadata cleaner. Re-encode a selected photo in your browser before sharing it.

## Features
- Select a local image and preview it
- Re-encode to JPEG, PNG, or WebP
- Adjustable JPEG/WebP quality
- Show original and output file sizes and image dimensions
- Download a separate cleaned copy; original remains untouched
- No upload endpoint, account, backend, or external dependency

## Run it
1. Download **Code → Download ZIP** and extract the folder.
2. Open `index.html` in a modern browser.
3. Select an image, choose the output format, then select **Clean & download**.

Optional local server: `python -m http.server 8000`, then visit `http://localhost:8000`.

## Important privacy note
The image is decoded and re-encoded locally using the browser canvas. This commonly removes metadata not preserved by the browser decoder/encoder, but format support varies. It is not a forensic guarantee that every metadata field has been removed. Verify the exported file with a trusted metadata inspector if the result is security-critical. Re-encoding can change image quality or transparency (JPEG does not support transparency).

## License
MIT — see [LICENSE](LICENSE).
