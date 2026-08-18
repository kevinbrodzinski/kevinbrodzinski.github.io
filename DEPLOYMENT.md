# kevinbrodzinski.com — Launch Package

This folder is the production web root. Deploy the **contents of this directory** to the root of your static hosting provider.

## Required before launch

1. Attach the custom domain `kevinbrodzinski.com` in your hosting provider.
2. Configure the DNS records exactly as your host specifies. Do not copy generic A/CNAME values from another provider.
3. Make `https://kevinbrodzinski.com/` the canonical hostname. Redirect `www.kevinbrodzinski.com` to the apex domain (or the reverse, if you later choose www) with a permanent redirect.
4. Enable automatic HTTPS/TLS and force HTTPS after the certificate is active.
5. Confirm these production URLs return `200`: `/`, `/favicon.svg`, `/apple-touch-icon.png`, `/og-image.png`, `/robots.txt`, `/sitemap.xml`, `/site.webmanifest`, and `/.well-known/security.txt`.
6. Test the site at desktop, tablet, and phone widths after deployment.
7. Verify the résumé download, command palette, recruiter mode, email link, and LinkedIn link on the live domain.
8. Confirm the social preview after deployment. Open Graph metadata points to `https://kevinbrodzinski.com/og-image.png`.
9. Submit `https://kevinbrodzinski.com/sitemap.xml` to Google Search Console after domain verification.

## Hosting notes

- The site has no runtime server dependency. `index.html` contains the interactive application and embedded résumé.
- `_headers` provides a conservative static-site security baseline on hosts that support that file (for example, Netlify/Cloudflare Pages-style deployments). If your provider ignores `_headers`, copy the equivalent headers into its configuration UI.
- Do not enable an aggressive Content Security Policy without retesting the in-page résumé download and canvas interactions. The supplied policy permits the current inline CSS/JS and Blob/Data operations used by the site.
- Do not add analytics before deciding which privacy posture you want. The launch package intentionally includes no third-party analytics or trackers.

## Canonical identity

- Public site: `https://kevinbrodzinski.com/`
- LinkedIn: `https://www.linkedin.com/in/kevin-brodzinski`
- Contact: `kevinpbrodzinski@gmail.com`

## Separate owned domains represented in the site

- `density.dev` — Enterprise Intelligence
- `tracescript.dev` — Adaptive Substrate Security
- `sensitivity.dev` — Response Intelligence
- `sphira.dev` — Verifiable Authorization

These are presented as portfolio/domain architecture. Only make them clickable from the main site once each destination has an intentional live experience or redirect.


## Visual atlas update

The `/research/` and `/patents/` routes use self-contained interactive SVG/CSS/JavaScript visual atlases. No additional runtime dependencies or build step are required.
