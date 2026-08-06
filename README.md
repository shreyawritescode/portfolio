# Shreya Mishra — Portfolio

A single-file, static HTML portfolio site for Shreya Mishra, Software Engineer at A.P. Moller-Maersk, focused on Apache Kafka, Kubernetes, and platform/streaming engineering.

**Live file:** [`shreya-mishra-portfolio.html`](shreya-mishra-portfolio.html)

## Overview

The entire site — markup, styles, and interactivity — lives in one self-contained HTML file (no build tools, bundlers, or external JS dependencies aside from Google Fonts). It ships with a light/dark theme toggle, scroll-triggered animations, and a small interactive "live pipeline" visualization built on `<canvas>`.

## Running it

No build step is required. Either:

- Double-click / open [`shreya-mishra-portfolio.html`](shreya-mishra-portfolio.html) directly in a browser, or
- Serve it locally for a more production-like experience (recommended, since some browsers restrict certain features on `file://` URLs):

  ```bash
  python3 -m http.server 8000
  ```

  then visit `http://localhost:8000/shreya-mishra-portfolio.html`.

## Page sections

Navigation (`#nav`) links to the following sections, in order:

| Section | Anchor | Description |
|---|---|---|
| Hero | — | Name, role, current employer, headline metrics |
| Live | `#live` | Interactive animated pipeline demo (Kafka-style throughput visualization) |
| About | `#about` | Engineering background across three lenses |
| Journey | `#journey` | Career timeline, intern → platform owner |
| Impact | `#impact` | Migration case study and quantified outcomes |
| Credentials | `#creds` | Certifications |
| Work | `#work` | Carousel of shipped/owned projects |
| Stack | `#stack` | Tools and technologies |
| Field Notes | `#field` | Conferences and community involvement (e.g. KubeCon, Kafka Summit) |
| Contact | `#contact` | Hiring/contact call-to-action |

## Customizing

Everything is inline in the single HTML file:

- **Theme colors** — CSS custom properties under `:root` (dark, default) and `html[data-theme="light"]` (light theme) near the top of the `<style>` block.
- **Fonts** — Sora (sans), Fraunces (display/serif), Space Mono (monospace), loaded from Google Fonts.
- **Content** — edit the corresponding `<section>` block directly; each section is clearly commented (`<!-- ===== SECTION ===== -->`).
- **Metrics/counters** — the animated numbers in the hero metrics strip use `data-count` attributes.

## Notes

- This is a static site — no server-side logic, no package manager, no dependencies to install.
- Not currently a git repository.
