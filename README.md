# Lin Liu — academic homepage

Static site for GitHub Pages. No build step, no dependencies.

```
index.html         home: about, news, research, selected publications, teaching, service, contact
publications.html  full publication list, grouped by year
style.css          all styling; edit the variables at the top to restyle the site
assets/            portrait and any PDFs (CV, papers)
```

## Editing

- **Photo** — replace `assets/portrait.svg` with a real photo, e.g. `assets/photo.jpg`,
  and update the `src` in `index.html` (`<img class="portrait" ...>`).
- **News** — add a `<li>` at the top of the `<ul class="news">` block in `index.html`.
- **Publications** — copy an existing `<li>` in `publications.html`. Wrap your own name in
  `<span class="me">L. Liu</span>` so it is highlighted.
- **Colours / fonts** — the `:root` block at the top of `style.css`. `--accent` is Tsinghua purple.
  Dark mode follows the reader's system setting and uses the same variables.
- **Add a CV** — drop `assets/cv.pdf` in and add a link in the `.links` row of `index.html`.

## Publishing

The site is served from the default branch of a `<username>.github.io` repository
(Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/`).

To update after editing:

```bash
git add -A && git commit -m "Update" && git push
```

Changes appear at `https://<username>.github.io/` within a minute or two.

## Accuracy note

Publication entries were compiled from DBLP and the Tsinghua faculty page. DBLP's
`Lin Liu 0001` record mixes in papers by other authors of the same name, so entries outside
the requirements/software/health line were left out. Add anything missing by copying an
existing list item.
