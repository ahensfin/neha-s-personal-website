# Portfolio site

A static site: `index.html` draws the mind map from `projects.json`. There is no server or build step.

## Files
- `projects.json`: your name, about text, the four branches, and every project
- `pdf/`: project PDFs. `pics/`: project thumbnails, plus `preview.png` (1200x630) for link previews
- `index.html`: the design. You rarely need to touch it

## Add a project (about 2 minutes)
1. Upload the PDF to `pdf/` and a thumbnail to `pics/` (on github.com: Add file, Upload files).
2. Open `projects.json`, click the pencil icon, and copy an entry in `projects`:

```json
{"id":"my-project","title":"My project","tags":["finance","cs"],
 "text":"Two or three sentences.","pdf":"pdf/my-project.pdf","img":"pics/my-project.png"}
```
- `id`: unique, letters, digits and hyphens only
- `tags`: any of `econ`, `finance`, `cs`, `personal`. The project links to every branch you list
- `img` and `pdf` are optional. Remove `"draft":true` once the text is real
3. Commit the change. The site updates in about a minute.

Watch the commas: a missing one breaks the page. Paste the file into jsonlint.com if it goes blank.

## Preview locally
Opening `index.html` by double-click will not load the JSON. From this folder run `python3 -m http.server 8000` and open http://localhost:8000.

## Deploy (free)
1. Create a GitHub account and a new public repo, then upload everything in this folder.
2. Repo Settings, Pages, deploy from the `main` branch, root folder. You get `username.github.io/repo`.
3. Custom domain (optional, about $10 to $15 a year): buy one, add it under Settings, Pages, and add the DNS records GitHub lists. HTTPS is automatic.

## Before you share it
- Replace the placeholder entries (marked `draft`) and add your last name in `projects.json`.
- Add `pics/preview.png` and your LinkedIn, email and résumé links.
- Get permission before posting research from your PREDOC work or Fed presentations, and never post restricted data.

## Later upgrades
- A git-based CMS (Decap or TinaCMS) gives you a form instead of editing JSON.
- A scheduled GitHub Action can pull Strava stats into `projects.json`.
