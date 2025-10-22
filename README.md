# MapOps — Why Page (GitHub Pages Ready)

This folder contains a single-file site (`index.html`) you can upload to GitHub and publish with GitHub Pages.

## Quick Publish (Project Site)
1. Create a new repo on GitHub (e.g., `MapOps-why`).
2. Upload `index.html` to the root of the repo (or push via git).
3. In **Settings → Pages**, set:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` (or `master`) and **Folder:** `/ (root)`
4. Click **Save**. Your site will appear at:
   `https://<your-username>.github.io/<your-repo>/`

## Quick Publish (User/Org Site)
If you want the site at `https://<your-username>.github.io/`:
1. Create a repo named exactly `<your-username>.github.io`.
2. Upload `index.html` to the root.
3. GitHub Pages will serve it automatically from the `main` (or `master`) branch.

## Custom Domain (Optional)
1. In **Settings → Pages**, add your domain (e.g., `mapops.dev`) in **Custom domain** and enable HTTPS.
2. In your DNS:
   - For **apex** domain (`mapops.dev`), create A records pointing to GitHub Pages IPs and AAAA records for IPv6 (see GitHub docs).
   - For **www** (`www.mapops.dev`), create a CNAME to `<your-username>.github.io`.
3. Add a file named `CNAME` in the repo root that contains only your domain (e.g., `mapops.dev`).

## Notes
- The original `<link rel="canonical">` and `<meta property="og:url">` tags were removed so previews/SEO won't point to the wrong domain when hosted under GitHub Pages.
- The embedded live map iframe points to fused.io and will work as-is.
- To change the contact email, search for `hello@mapops.dev` inside `index.html`.