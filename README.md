# data.olegmuratov.com — data-science portfolio site

A static site (plain HTML/CSS, no build step) for `data.olegmuratov.com`, hosted on **GitHub Pages**. Kept separate from the main Google Sites site at `olegmuratov.com`; it links *to* the main site, not the other way around.

## Files
- `index.html` — the whole site (self-contained; edit the Projects section to add work).
- `CNAME` — tells GitHub Pages the custom domain (`data.olegmuratov.com`). Don't delete.
- `.nojekyll` — tells Pages to serve files as-is (no Jekyll build).

## One-time setup (you do these — account/DNS actions)

**1. Create a public GitHub repo** (any name, e.g. `data-olegmuratov-com`) and add these files.
   - Easiest: on github.com → New repository → then "uploading an existing file" → drag in `index.html`, `CNAME`, `.nojekyll`, `README.md`.
   - Or via CLI:
     ```bash
     git init && git add . && git commit -m "Initial site"
     git branch -M main
     git remote add origin https://github.com/<your-username>/data-olegmuratov-com.git
     git push -u origin main
     ```

**2. Turn on GitHub Pages:** repo → Settings → Pages → Source = "Deploy from a branch" → Branch = `main` / `/ (root)` → Save.

**3. Set the custom domain:** same Pages screen → Custom domain → enter `data.olegmuratov.com` → Save. (The `CNAME` file already matches.)

**4. Add the DNS record** at whoever manages `olegmuratov.com`'s DNS (your registrar — likely where you set up the Google Sites domain):
   - Type: **CNAME** · Host/Name: **data** · Value/Target: **`<your-username>.github.io`**
   - This only adds the `data` subdomain; your apex `olegmuratov.com` and Google Sites stay untouched.

**5. Wait for DNS** (minutes to a few hours), then back on Settings → Pages, tick **Enforce HTTPS** once the certificate provisions.

## Adding a project
Open `index.html`, copy the commented TEMPLATE block in the Projects section, fill in the title/methods/links, and (for the Airbnb card) replace the "Coming soon" badge + placeholder with the real GitHub and writeup links.

## Note
Until at least one project is **live** (Airbnb), don't link this URL from your resume or share it — launch it with real content on it.
