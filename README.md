# Landing page draft

Working draft of a landing page. It is not a live offer and collects no data: the form has no backend. The page is marked `noindex`, both in the HTML and as an `X-Robots-Tag` header.

Static HTML and CSS, no build step. A Cloudflare Worker named `nosadia` serves `public/` as static assets at https://nosadia.com. Cloudflare redeploys it on every `git push` to `main`; `wrangler.jsonc` holds its settings, and the build log is in the dashboard under Workers & Pages → nosadia.

- `public/index.html`: the one page. A strict Content-Security-Policy blocks inline styles and scripts, so all styling lives in `public/style.css`.
- `public/_headers`: HTTP headers Cloudflare adds to every response (noindex, CSP, HSTS and other security headers). The file itself isn't served. Keep its CSP in step with the `<meta>` CSP in `index.html`.
- `public/img/`: everything the page shows. Every file in it is used.
- `public/og.png`: link preview image. `og:image` and `og:url` in `index.html` are absolute nosadia.com URLs.

Branch `gh-pages` serves the old draft address, https://chiguirito.github.io/uv-jacket-draft/, through GitHub Pages. Don't edit the page there: it only forwards visitors to nosadia.com.

How the images were made, and how to deploy and check: `../landing/image-pipeline/README.md`.
