Memory Album – Record → QR Template
====================================

Two ways to use:
1) DOWNLOAD MODE (no backend): Customer records, downloads a file like `demo-01.webm`, and you upload it later to `/audio/demo/01.webm`. You can then print QR codes pointing to `play.html?a=demo&t=01`.
2) FIREBASE MODE (one-time setup): Put your Firebase Storage keys in `assets/firebase-example.js`. The site uploads the recording directly and shows a QR that opens the player using `?file=<downloadURL>`.

Player accepts:
- Standard: `play.html?a=<albumId>&t=<trackNo>` → expects `/audio/<albumId>/<trackNo>.mp3|webm` on your host.
- Direct file: `play.html?file=<https://...>` → plays the exact URL (from Firebase or anywhere).

Pages:
- record.html – record in browser, preview, download, (optional) upload, get QR
- play.html – plays the audio
- tools/qr_sheet.html – prints QR codes for an album
