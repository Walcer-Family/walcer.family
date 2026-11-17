# walcer.family

Static site for walcer.family, served by GitHub Pages from the `main` branch root.

- `CNAME` sets the custom domain (apex `walcer.family`; `www` redirects to it).
- `.nojekyll` turns off Jekyll so dot-folders like `.well-known/` get published.
- `.well-known/matrix/client` and `server` let Matrix apps find the homeserver at
  `matrix.walcer.family` from a bare `@name:walcer.family` ID. Pages serves extensionless
  files as `application/octet-stream` with `Access-Control-Allow-Origin: *`; Matrix clients
  and servers parse the body as JSON regardless.

## DNS (Squarespace Domains)

| Host | Type | Value |
|---|---|---|
| @ | A | 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 |
| @ | AAAA | 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153 |
| www | CNAME | walcer-family.github.io |

Keep the existing MX, SPF, DMARC and the `matrix` / `tasks` CNAMEs.
