# STOURI × USR 2027 proposal (v12)

One self-contained page: fonts, images and code are all inside `index.html`. No build step, no server code.

| File | What it does |
|---|---|
| `index.html` | The proposal site (0.4 MB, about 0.1 MB compressed per visit) |
| `netlify.toml` | Tells Netlify to publish this folder as is, and keeps it out of search engines |
| `robots.txt` | Asks search engines not to index the site |
| `.gitignore` | Keeps Mac and Netlify clutter out of the repo |

## 1. GitHub
1. Create a new **private** repository (for example `stouri-usr-proposal`). Don't add a README.
2. Upload everything in this folder: **Add file > Upload files**, drag in all the files, then commit. `.gitignore` is hidden on a Mac: press Cmd+Shift+. in Finder to see it, or skip it.
   Or from a terminal inside this folder:
   ```
   git init && git add . && git commit -m "STOURI x USR proposal v12"
   git branch -M main
   git remote add origin https://github.com/<you>/stouri-usr-proposal.git
   git push -u origin main
   ```

## 2. Netlify
1. **Add new site > Import an existing project > GitHub**, then pick the repo.
2. Leave **Build command** empty. Set **Publish directory** to `.` (it's also in `netlify.toml`).
3. Click **Deploy**. Every push to `main` redeploys.

No GitHub? Use **Add new site > Deploy manually** and drag this folder in.

## Notes
- The site stays out of Google and other search engines (page tag, Netlify header and robots.txt). Anyone with the link can still open it.
- To ship a new version, replace `index.html` and push.
