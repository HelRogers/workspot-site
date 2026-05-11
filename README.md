# WorkSpot Ltd — website

A static Eleventy site for WorkSpot Ltd. Designed to be edited in Markdown and deployed to Netlify via GitHub.

## Quick start

```bash
npm install
npm start
```

The site will be available at `http://localhost:8080`.

To build for production:

```bash
npm run build
```

The output lands in `_site/`.

## Project structure

```
src/
├── _data/
│   ├── site.js          # Site-wide settings (title, email, social)
│   └── ventures.js      # List of businesses (edit this to add/remove ventures)
├── _includes/
│   ├── layouts/
│   │   └── base.njk     # Main HTML layout
│   └── partials/
│       ├── header.njk   # Site header and nav
│       └── footer.njk   # Site footer
├── assets/
│   ├── css/style.css    # All styles
│   └── images/          # Drop logo, favicon, og image here
├── index.njk            # Homepage
├── about.md             # About page (Markdown)
├── ventures.md          # Ventures page (Markdown)
├── contact.md           # Contact page with Netlify form
└── robots.txt
```

## Editing content

**Add or change a venture:** open `src/_data/ventures.js` and edit the list. The homepage and ventures page update automatically.

**Update contact details or site title:** edit `src/_data/site.js`.

**Edit a page:** open the corresponding `.md` file in `src/`. Markdown content sits below the frontmatter.

## Deploying to Netlify

1. Push the repo to GitHub.
2. In Netlify, click **Add new site → Import an existing project** and connect your GitHub repo.
3. Netlify reads `netlify.toml` so the build command and publish directory are already set.
4. Click **Deploy site**.

The contact form works automatically because of `data-netlify="true"` on the form. Submissions appear in your Netlify dashboard under **Forms**.

## Adding your real logo

Drop the WorkSpot logo PNG into `src/assets/images/` and update the header partial (`src/_includes/partials/header.njk`) to use it instead of the CSS-styled text logo. The text logo is there as a styled fallback that mirrors the branding.

## Custom domain

In Netlify, go to **Domain management → Add a domain** and follow the DNS instructions. Free HTTPS is automatic via Let's Encrypt.
