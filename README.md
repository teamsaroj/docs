# Porttera Docs

[![Docs Check](https://github.com/porttera/docs/actions/workflows/docs-check.yml/badge.svg)](https://github.com/porttera/docs/actions/workflows/docs-check.yml)

Documentation for Porttera Bundles, built with [Mintlify](https://mintlify.com).

## Structure

```
docs.json            # config: branding, colors, navigation
index.mdx            # home
faq.mdx
changelog.mdx
bundles/*.mdx        # installation, configuration, customization, features,
                      # how it works, uninstalling, troubleshooting
logo/                # wordmark logos (light/dark)
favicon.svg
```

## Preview locally

```bash
npm i -g mint        # install the Mintlify CLI
mint dev             # serve at http://localhost:3000
```

(If `mint` isn't found, `npx mint dev` also works.)

## Deploy

1. Push this repo to GitHub (`porttera/docs`).
2. In the [Mintlify dashboard](https://dashboard.mintlify.com), connect the repo.
   Mintlify auto-deploys on every push to `main`.
3. **Custom domain:** in the dashboard set the domain to `docs.porttera.com`,
   then add the CNAME it gives you at your DNS provider.

## Editing

Each page is an `.mdx` file with frontmatter (`title`, `description`) and Markdown +
Mintlify components (`<Card>`, `<Steps>`, `<Accordion>`, `<Note>`, `<Tip>`, `<Check>`).
Add a page by creating the file and listing its path in `docs.json` → `navigation`.
