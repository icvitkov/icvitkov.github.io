# icvitkov.github.io

Personal GitHub Pages site built with Nuxt 3.

## Requirements

- **Node.js** `>=16.10.0` (or `^14.18.0`; recommended: Node 18 LTS)
- **npm** `>=8`

## Key dependencies

| Package | Version |
|---------|---------|
| nuxt    | 3.6.5   |
| vue     | 3.3.4   |
| vite    | 4.4.7   |

## Setup

Install dependencies:

```bash
npm install
```

## Development

Start the dev server at `http://localhost:3000`:

```bash
npm run dev
```

## Deploying to GitHub Pages

This project uses [`gh-pages`](https://github.com/tschaub/gh-pages) to publish the static output to the `gh-pages` branch.

### First-time setup

1. Install `gh-pages` as a dev dependency:

```bash
npm install --save-dev gh-pages
```

2. Add a `deploy` script to `package.json`:

```json
"scripts": {
  "deploy": "nuxt generate && gh-pages -d .output/public"
}
```

> Nuxt's `nuxt generate` outputs the static site to `.output/public` by default.

3. Make sure **GitHub Pages** is configured to serve from the `gh-pages` branch in your repository settings (`Settings → Pages → Source: Deploy from a branch → gh-pages / root`).

### Publishing changes

Every time you want to push new changes live:

```bash
npm run deploy
```

This generates a fresh static build and force-pushes it to the `gh-pages` branch. The site is usually live within a minute or two.

### Notes

- The `gh-pages` branch is managed automatically — do not edit it manually.
- All source changes should be committed to `main` (or your default branch) before deploying.
- If your repo name is not `<username>.github.io`, set the base URL in `nuxt.config.ts`:

```ts
export default defineNuxtConfig({
  app: {
    baseURL: '/your-repo-name/'
  }
})
```
