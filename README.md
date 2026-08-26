# Frost Manifest

A freezer inventory tracker: add items, adjust quantities, scan a product's barcode
instead of typing it in, and see what's expiring soon.

`index.html` is the app, meant to be served as a static site (e.g. GitHub Pages) so real
camera access works for barcode scanning on every browser, iOS Safari included. It syncs
live across every device through a Firebase Realtime Database — see the setup comment
above `FIREBASE_CONFIG` near the top of the page's script for how to point it at your own
free Firebase project.

`legacy-artifact-version.html` is the earlier version built on the Claude Artifact
platform instead: no setup required and syncs instantly, but camera access is blocked
there at the platform level (confirmed on-device — no permission prompt ever appears, in
any browser), so barcode entry on that version is manual-only. Kept for reference in case
that tradeoff is ever preferable.
