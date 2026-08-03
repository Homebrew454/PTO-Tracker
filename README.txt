PTO TRACKER — PWA VERSION
=========================

This folder is a Progressive Web App (PWA): a "real" installable app icon,
its own window (no browser bar), and basic offline support — built from
the same dashboard as the standalone HTML file.

IMPORTANT — this needs to be hosted, not just double-clicked
--------------------------------------------------------------
Unlike the single standalone-HTML file, a PWA's "Install app" prompt and
offline caching only work when the files are served over http(s) — most
browsers block that functionality when you open a file straight off your
hard drive (file://). Opening index.html directly will still show the
dashboard and work fine, it just won't offer to install as an app or work
offline.

To get the full installable experience, put this whole folder somewhere
reachable by a URL. Easiest free options:

  1. GitHub Pages — create a public repo, upload this folder's contents,
     turn on Pages in repo settings. You'll get a URL like
     https://yourname.github.io/pto-tracker/
  2. Netlify Drop (app.netlify.com/drop) — drag this folder in, get an
     instant URL, no account required for a quick test.
  3. Your company's intranet/static file server, if you have one and IT
     allows it.

Once it's hosted, open that URL on your phone:
  - Chrome (Android): menu (⋮) → "Install app"
  - Safari (iPhone):  Share icon → "Add to Home Screen"
It will then behave like a normal app icon — its own window, no address
bar, and it'll keep working (mostly) if you lose signal.

Files in this folder
---------------------
  index.html        the app itself
  manifest.json      tells the browser the app's name/icon/colors
  service-worker.js  enables offline caching of the app shell
  icons/              app icons at the sizes browsers expect

Data behavior is unchanged from the standalone HTML version: everything
is stored locally in that browser/installation only, nothing syncs
between devices, and Export/Import (top-right buttons in the app) is
still the way to back up or move your data.
