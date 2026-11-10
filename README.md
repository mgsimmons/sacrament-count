# Sacrament Count

A small web app for counting Sacrament meeting attendance on an iPhone, section by section.

**Live app:** https://mgsimmons.github.io/sacrament-count/

## Use it

1. Open the link in Safari on your iPhone.
2. Tap the Share button, then **Add to Home Screen**. It opens full screen like a regular app and works offline.
3. Tap a section (Stand, Left Side, Middle, Right Side, Back Row, Overflow, Foyers), then tap **+** or **−**.
   Tap the selected section again to type its subtotal.
4. **Copy total** puts the total on the clipboard. **Save Sunday** keeps that Sunday's breakdown under History.

Counts and history are stored only on the phone that recorded them (browser local storage). Nothing is sent anywhere.
Deleting the Home Screen app or clearing Safari website data erases the history.

## How it's built

- `index.html`: the whole app (HTML, CSS, and JavaScript, no build step).
- `sw.js`: service worker that caches the app so it opens with no signal. Bump `CACHE` when you change `index.html`.
- `manifest.webmanifest` and `icons/`: Home Screen name and icon.

Hosted with GitHub Pages from the `main` branch.
