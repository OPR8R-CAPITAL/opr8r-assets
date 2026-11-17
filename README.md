# opr8r-assets

Public brand assets served at https://assets.opr8r.capital - logos and images referenced by email signatures and external documents. Public by design: nothing confidential here.

## What belongs here

Only files that must be fetched by URL: by an email client, by a web page, or by a third party outside OPR8R who needs the current version without being sent files.

Everything else stays in the Brand Library. No source files, no print masters (EPS, AI), no personal data, no QR codes containing phone numbers, no client material. Assume anything committed here is permanent, indexed and scraped, including after deletion.

## Files

| File | Use |
|---|---|
| `opr8r-signature.png` | The logo in the email signatures. Do not rename or move - the installed signatures reference this exact path. |
| `opr8r-logo-136.png` / `-272.png` / `-408.png` | Flagship mark, 1x / 2x / 3x, for HTML email and documents |
| `opr8r-logo-horizontal.svg` | Horizontal lockup, scalable |
| `opr8r-logo-vertical.svg` | Vertical lockup, scalable |
| `opr8r-logo-icon.svg` | Shield only, scalable |
| `opr8r-powered-by-horizontal.svg` / `-4096.png` | Powered By, horizontal - for sponsors and partners |
| `opr8r-powered-by-vertical.svg` / `-4096.png` | Powered By, vertical |
| `opr8r-powered-by-shield.svg` / `-4096.png` | Powered By, shield |
| `opr8r-powered-by-inline.svg` / `-4096.png` | Powered By, inline |

Reference a file as `https://assets.opr8r.capital/<filename>`.

## How it is served

GitHub Pages from `main` at the repository root, on the custom domain `assets.opr8r.capital`, with Enforce HTTPS on.

The Cloudflare CNAME `assets` to `opr8r-capital.github.io` is deliberately **DNS only** (grey cloud). Cloudflare Workers run only on proxied hostnames, so a DNS-only record routes straight to GitHub Pages and the site's launch gate never sees the request. Turning the cloud orange would put the gate in front of these files and break them for external recipients.

To add an asset: commit it to the repository root. It is served within about a minute.
