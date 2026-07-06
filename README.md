# Makerspace Wiki

Source for our makerspace's tool & equipment wiki, built with [MkDocs](https://www.mkdocs.org/) + the [Material theme](https://squidfunk.github.io/mkdocs-material/), version-controlled in this repo, and published with GitHub Pages.

## Structure

```
docs/
  index.md              Home page / navigation hub
  cnc.md                CNC machines, software, materials, tool settings, safety, FAQ
  lasercutters.md        Laser cutters, software, materials, tool settings, safety, FAQ
  3d-printers.md          3D printers, software, safety, FAQ
  woodworking.md          Woodworking/carpentry tools, safety, FAQ
  sewing.md               Sewing machines, safety, FAQ
  electronics.md          Electronics bench equipment, safety, FAQ
  img/                    (create as needed) images referenced from pages
mkdocs.yml               Site config and navigation
```

## Editing (admins only: [you + partner + helpers])

1. Clone the repo.
2. Install MkDocs Material once: `pip install mkdocs-material`
3. Preview locally: `mkdocs serve` then open `http://127.0.0.1:8000`
4. Edit the relevant `.md` file under `docs/`. Each page uses `##` for subcategories (Machines, Software, Materials, Tool Settings, Safety, FAQ) and `###` for each individual machine/software entry — keep that pattern so the table of contents stays consistent.
5. To add images: drop the file in `docs/img/` and reference it with `![alt text](img/filename.jpg)`.
6. Commit and push to `main` — the GitHub Action in `.github/workflows/deploy.yml` will automatically rebuild and publish the site to GitHub Pages.

## First-time setup checklist

- [ ] Create a new GitHub repo and push this folder to it.
- [ ] In the repo, go to **Settings → Pages** and set the source to **GitHub Actions**.
- [ ] Update `site_url` in `mkdocs.yml` once you know the Pages URL (or your custom domain).
- [ ] Add your partner/helpers as **Collaborators** with **Write** access under **Settings → Collaborators** (keep the repo public, or use "Deploy from a branch" visibility settings, so members can read without needing GitHub accounts).
- [ ] Replace the placeholder text (in `[brackets]` and under `_italic prompts_`) in each page with real info — specs, locations, training requirements, actual FAQ content.
- [ ] If you want a custom domain (e.g. `wiki.yourmakerspace.org`), add a `docs/CNAME` file containing that domain and configure DNS per [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Access model

- **Read access:** anyone (repo/site is public).
- **Write access:** only GitHub collaborators you explicitly add (you, your partner, and up to 2 helpers). Members can suggest edits by opening an Issue or Pull Request, but can't push directly.
