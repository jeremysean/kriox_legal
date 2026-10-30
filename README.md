# Kriox legal pages

Public home page, Privacy Policy and Terms of Service for Kriox, an AI-assisted purchasing and goods-receipt
assistant. The pages are the links required by the Google Cloud OAuth consent screen (Google Auth Platform, Branding)
for the Kriox Gmail integration.

The application code lives in a separate private repository. This repository holds only static pages.

## Contents

| File | Purpose |
|---|---|
| `index.html` | Application home page |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Service |
| `style.css` | Shared styles (light and dark) |
| `logo.svg` | Kriox logo and page icon |

Plain HTML and CSS. There is no build step and no JavaScript. Links between pages are relative, so the site works
under a repository sub-path such as `/kriox_legal/`.

## Publishing

Hosted with GitHub Pages from the root of the `main` branch (Settings, Pages, Source: Deploy from a branch, branch
`main`, folder `/ (root)`), at <https://jeremysean.github.io/kriox_legal/>.

## Google Cloud configuration

In the Google Cloud console, Google Auth Platform, Branding:

| Field | Value |
|---|---|
| Application home page | `https://jeremysean.github.io/kriox_legal/` |
| Application privacy policy link | `https://jeremysean.github.io/kriox_legal/privacy.html` |
| Application terms of service link | `https://jeremysean.github.io/kriox_legal/terms.html` |
| Authorized domains | `jeremysean.github.io` |

Google requires the privacy policy to be on the same domain as the home page, and each authorized domain to be
verified in [Google Search Console](https://search.google.com/search-console) (URL-prefix property, HTML-file
method: add the file Search Console provides to the repository root and push it).

## Keeping the pages accurate

The Privacy Policy describes what the Kriox Gmail poller does. Update it, and the "Last updated" date in both
policy pages, whenever that behaviour changes, in particular:

- the Gmail scope requested (currently `gmail.modify`);
- which messages are kept or labelled;
- the AI and cloud services that process message content;
- the storage region or retention.

The contact address appears in the footer of every page, in the introduction and section 7 of the Privacy Policy, and
in section 11 of the Terms of Service.
