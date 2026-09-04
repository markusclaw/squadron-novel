# Deploying SQUADRON to Cloudflare Pages

Two paths. **Option A** gets you live in ~2 minutes with no git and no working
terminal. **Option B** is the permanent setup that auto-rebuilds every time you push.

---

## Option A — Direct Upload (fastest, no git needed)

Use the pre-built site zip: **`squadron-site-dist.zip`** (this is the already-compiled
static website — the contents of the `site/` folder).

1. Unzip `squadron-site-dist.zip` on your Mac (double-click in Finder). You'll get a
   folder of files including `index.html`.
2. Go to the Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** →
   **Upload assets**.
3. Name the project (e.g. `squadron`), then **drag the unzipped folder** (the one
   containing `index.html`) into the upload area.
4. Click **Deploy site**. Cloudflare gives you a live URL like
   `https://squadron.pages.dev` within about a minute.

That's it — the site is live. To update it later this way, rebuild and re-upload. For
automatic updates, set up Option B.

---

## Option B — Connect the GitHub repo (auto-rebuild on every push)

This makes the site rebuild automatically whenever `main` changes — the intended
long-term workflow. It requires the repo to be pushed to GitHub first.

1. Push this repository to `github.com/markusclaw/squadron-novel` (see the git steps in
   the delivery notes, or below).
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to
   Git** → pick `markusclaw/squadron-novel`.
3. Set the build configuration:

   | Setting | Value |
   |---------|-------|
   | Framework preset | None |
   | Build command | `pip install -r requirements.txt && mkdocs build` |
   | Build output directory | `site` |
   | Environment variable | `PYTHON_VERSION` = `3.11` |

4. **Save and Deploy.** From now on, every push to `main` triggers a rebuild.

### Git steps (run these once your Mac's terminal is working again)

```bash
cd ~/Documents/squadron-novel
git add -A
git commit -m "story+site: Foundation v0.2 repository and reading site"
git push origin main
```

---

## Local preview (optional)

```bash
pip install -r requirements.txt
mkdocs serve      # live preview at http://127.0.0.1:8000
```

## Housekeeping

These earlier empty template files at the repo root are **superseded** by the new
structure and can be removed whenever convenient:

```
OUTLINE.md   CHARACTERS.md   WORLDBUILDING.md   TIMELINE.md
```

`FOUNDATIONS.md` (the craft foundations doc) has been folded into
`docs/foundation/foundation_v0.2.md`; keep it or delete it as you like.

Set `site_url` in `mkdocs.yml` to your real Cloudflare URL once you have it.
