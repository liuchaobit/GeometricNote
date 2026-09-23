# GeometricNote

> A personal academic wiki on **differential geometry** and **geometric / theoretical control theory**.

## What's inside

- `index.html` — the wiki home page (self-contained, KaTeX-rendered).
- `notes/` — markdown source notes.
  - `differential-geometry/` — manifolds, tangent spaces, Lie groups & algebras, differential forms, connections.
  - `geometric-control/` — affine control systems, distributions, Frobenius, controllability Lie algebra, optimal control.

## Publish with GitHub Pages

1. Push to `main`.
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
3. Wait ~1 minute; the site goes live at `https://liuchaobit.github.io/GeometricNote/`.

## Adding a note

- Drop a `.md` file under `notes/<topic>/`.
- Add a matching `<a data-page="...">` in `index.html` and a `<section class="page">`.
- Use `$...$` for inline math and `$$...$$` for display math (KaTeX).
