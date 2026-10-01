# Girish Konda

Personal portfolio for [girishkonda.com](https://girishkonda.com/), hosted on GitHub Pages.

A text-first personal profile built with HTML and CSS, with a responsive layout.
No build step, runtime framework, or external fonts are required. Reading and
navigating the site do not depend on JavaScript. A single optional Cloudflare
Web Analytics beacon collects site-wide traffic measurements.

## Preview locally

From this directory:

```powershell
python -m http.server 8080 --bind 127.0.0.1
```

Open `http://127.0.0.1:8080`.

The analytics hostname is `girishkonda.com`, not localhost. Local previews are
not production traffic; an analytics hostname/CORS rejection does not prevent
the page from working.

## Traffic analytics

Cloudflare Web Analytics is installed manually using its non-blocking module
snippet in `index.html`. The value in `data-cf-beacon` is a public website
identifier, not an account login or API credential.

- The website stays on GitHub Pages. Nameservers stay at Spaceship.
- Do not enable a Cloudflare proxy, WAF, Bot Fight Mode, Turnstile, or visitor
  challenge as part of this analytics setup.
- Analytics being blocked or unavailable must not block access to the page.
- Measurements cover visits and pageviews from direct, search, social, and
  other entry routes, starting when the beacon was deployed.
- Ad blockers, disabled JavaScript, and failed beacon requests can cause
  undercounting. These are not complete server-access logs or unique-person counts.
- Cloudflare does not currently log query strings or support UTM/custom-event
  reporting. Keep the existing Short.io event links for QR-versus-printed-route
  counts; do not treat those redirect counts as identical to site pageviews.
- Cloudflare documents seven days of unsampled beacon retention, sampled or
  aggregated reporting, and access to the previous six months of data. Export
  reports when a longer record is needed.

References: [manual setup](https://developers.cloudflare.com/web-analytics/get-started/#sites-not-proxied-through-cloudflare)
and [coverage, sampling, and retention](https://developers.cloudflare.com/web-analytics/faq/).

## Update the site

- Edit `index.html` for the biography, work experience, education, projects,
  contributions, standards/community participation, talks, and reviewing or judging.
- The public contact address is `hello@girishkonda.com`, linked with `mailto:`
  in the Contact section. Other mailbox addresses require separate approval.
- Stack contact links in Email, LinkedIn, and GitHub groups, with each link on
  its own line and both GitHub profiles together.
- Edit `styles.css` for layout and presentation.
- Update `favicon.svg` for the site icon.
- Keep claims and contribution statuses supported by their linked public sources.
- Distinguish confirmed talks from submitted proposals, and workshop reviewing
  from main-conference reviewing. Do not describe a reviewer-pool registration
  or an application as completed professional service.
- Keep review invitations distinct from accepted assignments or completed reviews.
  Do not publish manuscript titles, review-system links, or confidential review material.
- Keep reviewer entries brief: venue, role, year, and at most a short topic
  description. Leave out review counts, submission dates, and process detail.
- Distinguish community participation and open contributions from formal governance
  roles, maintainership, or merged work. Recheck linked PR statuses when updating.
- Verify the publisher and repository of a package listing before linking to it.
- Employment headings contain company names; teams and organizations belong in
  the descriptions. Use the resume to check facts, roles, and dates, not as copy
  to paste. Write short personal summaries rather than an achievement-bullet inventory.
- Do not add unverified revenue, financial, or customer details.
- Keep PR links together in Standards & communities, with visible labels in
  `#number` format and descriptive accessible labels.
- Link speaking appearances to the actual session/speaker page, and link Usher
  to its official VS Code and Edge listings.
- Do not add private documents, credentials, unpublished manuscripts, or personal
  contact details that have not been approved for publication.

## GitHub Pages

Publish the `main` branch from the repository root. The `.nojekyll` file tells
GitHub Pages to serve the files without Jekyll processing.

The `CNAME` file declares `girishkonda.com` as the custom domain. The canonical
and Open Graph URLs in `index.html`, the sitemap location in `robots.txt`, and
the URL in `sitemap.xml` must use the same domain.

Configure the custom domain in GitHub Pages before pointing DNS at GitHub.
The apex domain uses GitHub Pages' published A records; `www` is a CNAME to
`girishkvs.github.io`. Preserve unrelated DNS records and enforce HTTPS once
the certificate is ready.
