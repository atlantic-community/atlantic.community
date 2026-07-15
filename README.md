# Atlantic Community

Minimal Astro website for [atlantic.community](https://atlantic.community), deployed with Cloudflare Workers Static Assets.

## Development

Requires Node.js 22.12+ and pnpm 10.

```sh
pnpm install
pnpm astro dev --background
```

The site runs at [http://localhost:4321](http://localhost:4321). Manage the background server with:

```sh
pnpm astro dev status
pnpm astro dev logs
pnpm astro dev stop
```

## Build

```sh
pnpm build
pnpm preview
```

Astro generates the static site in `dist/`, including the custom 404 page and sitemap.

## Deployment

Cloudflare builds and deploys every push to `main` using:

- Build command: `pnpm run build`
- Deploy command: `npx wrangler deploy`

`wrangler.jsonc` serves `dist/` as static assets and routes both `atlantic.community` and `www.atlantic.community` to the Worker.

To deploy manually:

```sh
pnpm deploy
```
