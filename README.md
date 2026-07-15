# Atlantic Community

Minimal static Astro site for [atlantic.community](https://atlantic.community), deployed with Cloudflare Workers Static Assets.

## Development

```sh
pnpm install
pnpm astro dev --background
```

Use `pnpm astro dev status`, `pnpm astro dev logs`, and `pnpm astro dev stop` to manage the background server.

## Deployment

Cloudflare builds the site with `pnpm run build` and deploys it with `npx wrangler deploy`. The Worker serves the generated `dist` directory as static assets and uses `dist/404.html` for missing routes.
