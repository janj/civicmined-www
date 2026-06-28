# civicmined.org — landing page

Static landing page served at the apex domain **civicmined.org** via GitHub Pages.
City instances live on their own subdomains (`petaluma.civicmined.org`, etc.) and
are deployed separately from the [civic-mined](https://github.com/janj/civic-mined)
platform repo on Fly.io — this repo is *only* the public splash page.

## Editing

It's a single self-contained `index.html` (no build step). Edit and push to `main`;
GitHub Pages redeploys automatically.

## DNS (apex domain)

The apex `civicmined.org` cannot be a CNAME, so it uses A/AAAA records to GitHub's
Pages IPs (set at the registrar):

```
@   A      185.199.108.153
@   A      185.199.109.153
@   A      185.199.110.153
@   A      185.199.111.153
@   AAAA   2606:50c0:8000::153
@   AAAA   2606:50c0:8001::153
@   AAAA   2606:50c0:8002::153
@   AAAA   2606:50c0:8003::153
```

`www.civicmined.org` can optionally CNAME to `janj.github.io`.

The `CNAME` file in this repo pins the custom domain; don't delete it.
