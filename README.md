# Landing page draft

Working draft of a landing page. It is not a live offer and collects no data: the form has no backend. The page is marked `noindex`.

Static HTML and CSS, served by GitHub Pages from `main`. No build step.

- `index.html`: the one page. A strict Content-Security-Policy blocks inline styles and scripts, so all styling lives in `style.css`.
- `img/`: everything the page shows. Every file in it is used.
- `og.png`: link preview image.
- `v2/index.html`: forwards to the root. Version 2 became the page on 2026-11-07, and this keeps old links working.

How the images were made, and how to deploy and check: `../landing/image-pipeline/README.md`.
