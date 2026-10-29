# bobsnoodlefactory.com

The website for **Bob's Noodle Factory LLC**: one page saying who the studio is, what it has shipped
(Vantage Point), how the work runs, and how to get in touch.

Plain HTML and CSS. No build step, no scripts, no cookies, no analytics, nothing from anyone else.

## Look at it

Open `index.html` in a browser. It follows the computer's light or dark setting.

## What's here

| File | What |
|---|---|
| `index.html` | The page. All the words live here. |
| `404.html` | What someone sees at an address that doesn't exist. |
| `site.css` | The look: warm paper, broth-dark ink, chili red. Colours are set once at the top. |
| `favicon.svg` | The bowl icon in the browser tab. |
| `img/vantage-point.png` | Vantage Point's app icon, from getvantagepoint.app. |
| `CNAME` | Tells GitHub Pages which domain to answer to. |
| `saturday/index.html` | A passcode-locked scheduling tool (not linked from the site). See below. |

## This repo is public

Nothing private goes in here — no client work, no confidential material, no addresses. Every line on
the page has to be true; facts about Vantage Point come from its own site, getvantagepoint.app.

## How it's served

GitHub Pages from the `main` branch, at `bobsnoodlefactory.com` (domain and email forwarding at
Porkbun; `rob@bobsnoodlefactory.com` forwards to Gmail). **Pushing to `main` is the go-live action:**
every change is live a minute later.

Porkbun DNS records for the site (the MX and TXT records are the email forwarding — leave them alone):

| Type | Host | Answer |
|---|---|---|
| A | (blank) | 185.199.108.153 |
| A | (blank) | 185.199.109.153 |
| A | (blank) | 185.199.110.153 |
| A | (blank) | 185.199.111.153 |
| CNAME | www | bigskybob.github.io |

## /saturday

`bobsnoodlefactory.com/saturday` hosts a private scheduling tool, locked behind a passcode. It is the
one page on this site with scripts, and it isn't linked from anywhere else. The page is encrypted:
without the passcode the file is unreadable. Nothing anyone types into it is sent anywhere; boards stay
in that viewer's browser or in files they save themselves. The source and the build that encrypts it
live outside this repo, so updates arrive here as a new `saturday/index.html`.
