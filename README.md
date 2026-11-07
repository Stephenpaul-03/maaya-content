# Maaya Stores content

This is the independent `content repo (remote not configured)` content repository. Its sibling `website` repository contains the Next.js application, local editors, schemas and validation tools.

- `content/*.json`: editable website, bookstore and stationery content.
- `book-covers/manifest.json` and referenced images: cached book covers.
- `.github/workflows/rebuild-website.yml`: requests a website rebuild after content pushes.

From `../website`, run `npm run edit:text` or `npm run edit:content`. Saving changes files here directly. Run `npm run content:publish` there to validate and publish; direct Git commits here are also supported. Run `npm run content:prepare` in the website after direct JSON edits to refresh its build snapshot. The website field reference is `website/src/content/README.md`.

For automatic public website rebuilding, configure `WEBSITE_DISPATCH_TOKEN` in this repository's Actions secrets, scoped to the website repo. Never commit credentials. The website workflow must read this repository at build time.

Remote: `git@github-personal:Stephenpaul-03/maaya-content.git`. Website: `Stephenpaul-03/maaya-website`.
