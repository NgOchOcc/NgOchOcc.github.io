# Ngoc Luu — Academic Portfolio

Personal academic homepage of **Ngoc Luu**, AI researcher at Qualcomm AI Research.
A single static page in a "technical drawing / blueprint" design language — no framework, no build step.

## Structure

```
index.html      the entire site (HTML + CSS + a little vanilla JS)
404.html        not-found page
assets/         downloadable résumé
.nojekyll       tells GitHub Pages to serve files as-is
```

## Publishing changes

```bash
git add -A && git commit -m "update" && git push
```

The site refreshes a minute or so after pushing to `main`.

## Everyday maintenance

- **New paper** — copy an existing `<div class="pub">…</div>` block inside `<div class="publist">`,
  edit title / authors / tag / links, and add `data-fa="1"` if first-author (feeds the sort toggle).
  Add its hand-drawn fallback by copying a `<svg class="thumb">` sketch, or just let it show the figure.
- **New figure** — replace a publication's inline thumbnail SVG or add a normal image.
- **Highlights** — add an `<li>` at the top of `<ol class="news">`.
- **Under-review paper gets accepted** — swap its `vtag` text to the venue, delete the red
  `<span class="stamp">` and update the arXiv links if needed.
- **Update the résumé** — replace `assets/Ngoc_Luu_Resume.pdf` while keeping the filename.
- **Title-block revision tag** — bump `REV B` / date in the footer title block when you feel like it. :)

## Local preview

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

(Opening index.html via file:// also works; remote-fallback images need network.)

## Design notes

Palette: white paper, graphite ink, sage board, and cobalt technical marks.
Type: Geist + Geist Mono + Lora.
The page is a tracing sheet taped over graph paper: index flags on the right edge are fixed
navigation with scroll-spy; on narrow screens they re-mount along the top edge.
