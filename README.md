# AOP — Creative Agency Website (case study)

> 🌐 **Live: [aopcreativeagency.com](https://aopcreativeagency.com/)**
>
> Designed and built by **Ahmet Yusuf Bursal**. The source code belongs to the
> client and is not public; this repository documents the work.

**AOP** is an Istanbul-based advertising, creative communication and events
agency whose identity blends Anatolian craft (ebru, kilim, embroidery) with
today's music, street and club culture. I built the agency's portfolio site
from brand discovery to deployment.

## My role

Everything on the web side: brand-asset review, site flow and storyboard,
motion design in code, front-end build, performance work, deployment and the
private preview environment.

## What the site does

- **Animated logo intro** — the brand's star "marbles" like ebru, opens at the
  centre, gathers itself and reveals the stage
- **Full-screen hero film** that shrinks into the home screen after the intro
- **One continuous vertical composition** instead of hard section jumps:
  sticky areas, scroll-linked colour transitions between sections, glitch
  headline changes
- Sections: story, grouped services, experience, music & culture, contact
- Strict brand system: fixed palette (#0000D1 · #FA0401 · #6DF949 · #000 · #FCFCF2),
  Extenda + IBM Plex Mono typography, motifs used as structure rather than decoration
- Contact form via serverless function, KVKK privacy notice page

## Engineering

- Hand-written **HTML / CSS / vanilla JavaScript** — no framework, so every
  animation is tuned frame by frame
- Separate modules for intro, logo motion, headline, story, works, menu and
  smooth scrolling
- Image pipeline to responsive **WebP** sets; long-lived caching for fonts,
  day-long caching for media, revalidation for HTML/CSS/JS
- **Password-protected client preview** on Netlify: an edge function gates
  every path, credentials live only in environment variables, sessions use a
  hashed cookie, and the site fails *closed* if configuration is missing
- Release script that builds a clean deploy folder (no drafts, backups or
  review pages); `noindex` headers on preview builds

## Status

Live at [aopcreativeagency.com](https://aopcreativeagency.com/). Built with a
password-protected preview for client review, then launched to production.
