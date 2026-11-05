# CometCMS documentation

This repository contains the VitePress documentation for CometCMS.

## Local development

Use Node.js 24 and install the locked dependencies:

```sh
npm ci
npm run dev
```

Build and preview the production site:

```sh
npm run build
npm run preview
```

The generated site is in `.vitepress/dist`.

## GitHub Pages

1. Open this repository's **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
2. Push the workflow to `main`. Every push to `main` builds and deploys the documentation. You can also run **Deploy documentation to GitHub Pages** manually from the **Actions** tab, using the `main` branch.
3. After a successful deployment, the site is available at <https://cometcms.github.io/documentation/>.

The workflow uses the built-in `GITHUB_TOKEN`; no additional secrets or `gh-pages` branch are required. If the `github-pages` environment has deployment protection rules, allow deployments from `main`.

The `base` setting in `.vitepress/config.js` matches the repository path, `/documentation/`. Update it if the repository is renamed, or set it to `/` when serving the site at the root of a custom domain.

See [GitHub's Pages publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) for the repository setting.
