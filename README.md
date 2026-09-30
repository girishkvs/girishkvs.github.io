# Girish Konda

Personal portfolio for [girishkvs.github.io](https://girishkvs.github.io/).

A text-first personal profile built with HTML and CSS, with a responsive layout.
No build step, JavaScript
runtime, external fonts, analytics, or third-party dependencies are required.

## Preview locally

From this directory:

```powershell
python -m http.server 8080 --bind 127.0.0.1
```

Open `http://127.0.0.1:8080`.

## Update the site

- Edit `index.html` for the biography, work experience, education, projects,
  contributions, standards/community participation, talks, and reviewing or judging.
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

When connecting a custom domain, update the canonical and Open Graph URLs in
`index.html`, the sitemap location in `robots.txt`, and the URL in `sitemap.xml`.
Configure and verify the domain through GitHub Pages before changing DNS.
