# Primus Invest &ndash; website

Static one-page site for Primus Invest (Johan Siwers), hosted for free on GitHub Pages
with the custom domain `www.primusinvest.se`.

No build step: plain HTML/CSS/JS. Open [index.html](index.html) directly in a browser
to preview, or run a local server, e.g. `python3 -m http.server` from this folder.

## What still needs to be filled in

Search the code for `TODO` to find every spot, or use this list:

- **Images** &ndash; three placeholders are currently styled gray boxes:
  - `hero-image` in `index.html` (Start section) &rarr; the Chamonix shopfront photo.
  - `about-portrait` in `index.html` (Om Johan section) &rarr; a portrait of Johan.
  - The mountain + flame symbol is a simple placeholder SVG (`assets/favicon.svg` and
    the inline `#primus-mark` symbol in `index.html`) standing in for the final logo.
- **Engagemang section** &ndash; each card (Recapex, PRJM, PES, Norrstigen, DHS Venture
  Partners, Supermarket.vc, J12) has a placeholder sentence and a `#` link.
- **LinkedIn link** &ndash; the Kontakt section's LinkedIn button points to `#`.
- **Org.nr** &ndash; the footer has `org.nr [fyll i]`.

## Domain setup (replaces the Google Sites steps in the brief)

The original brief pointed `www.primusinvest.se` at Google Sites. Since this is hosted
on GitHub Pages instead, give NMU these DNS records instead of the Google Sites ones:

| Type | Name | Value |
|---|---|---|
| CNAME | `www` | `siwwan.github.io` |

And forward the bare domain `primusinvest.se` (no www) to `https://www.primusinvest.se`,
same as the original plan. The Google Workspace email records (MX, SPF, DKIM, DMARC)
from the brief are unaffected &ndash; those stay exactly as planned, since email and web
hosting are independent.

After DNS propagates (usually under an hour, sometimes up to a day), GitHub Pages will
issue an HTTPS certificate for the domain automatically.

## Deploying changes

Any push to the `main` branch republishes the live site automatically via GitHub Pages
(no workflow/build step needed &ndash; it serves the static files directly).
