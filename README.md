# Lita's memorial site

Lita's memorial page, hosted as a plain static site on Cloudflare (free plan). There's no server code or database to manage; Cloudflare just serves the page and its photos.

## What's in this folder

| File | What it is |
|---|---|
| `page.html` | The page itself. Edit this one. `build.ps1` turns it into `public/index.html`. |
| `public/` | What visitors download: `index.html` (built) and `photos/`. |
| `wrangler.jsonc` | Cloudflare settings. |

## Preview on this computer

```
npm run dev
```

Open http://127.0.0.1:8787. Press `Ctrl+C` to stop.

## Updating the live site

Edit `page.html` (text, schedule, captions), add any new photos to `public/photos/`, then:

```
npm run deploy
```

The new version is live within a few seconds. If it asks you to log in, run `npx wrangler login` first.

## Optional: your own address

To use a domain like `litabayari.com`, add it in Cloudflare under Workers & Pages → `lita-tribute` → Settings → Domains & Routes.
