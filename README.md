# spero-web

The site for [spero-technologies.com](https://spero-technologies.com).

Static HTML and CSS, no build step. Everything served lives in `src/`.

## Local preview

```sh
python3 -m http.server -d src 8000
```

Then open http://localhost:8000.

## Deploying

Pushes to `main` deploy automatically via Workers Builds (Worker `spero`).

There is no build step. `wrangler.jsonc` points the assets directory at `src/`,
so the default deploy command (`npx wrangler deploy`) is all that's needed.
