# boredscanner.space

Static site for Bored Scanner. No build step, no JavaScript, no analytics.
Served by GitHub Pages from `main`. Same layout and stylesheet as boredpackage.space and boredguest.space; the palette tokens at the top of `style.css` differ, and the hero uses a phone mock (`.phone`) instead of the iPad `.screen`.
Icons come from the Bored Scanner asset kit (`Web/`). `privacy.html` is the App Store privacy policy URL.

## Fonts and Content-Security-Policy

Instrument Sans is self-hosted in `fonts/` (`@font-face` at the top of `style.css`, licence in `fonts/OFL.txt`); the site makes no third-party requests. Every page has a `Content-Security-Policy` meta tag (`default-src 'self'`, no scripts), so inline `style=` attributes and `<style>` blocks are blocked: add a class in `style.css` instead (one-off tweaks are the `u-` classes at the bottom). New pages need the same meta tag.
