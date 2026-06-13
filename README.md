# yueyvettehao.github.io

Personal portfolio built with [Hugo](https://gohugo.io) and the [Tranquilpeak theme](https://github.com/kakawait/hugo-tranquilpeak-theme), auto-deployed to GitHub Pages via GitHub Actions.

## First-time setup (one time only)

1. Create a GitHub repo named **`YueYvetteHao.github.io`** (public).
2. Push this folder:
   ```bash
   git remote add origin git@github.com:YueYvetteHao/YueYvetteHao.github.io.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source = "GitHub Actions"**.
4. Wait ~2 min for the Action to finish. Site is live at <https://yueyvettehao.github.io>.

## Writing posts

Add a markdown file to `content/posts/`, commit, push. Done — GitHub Actions rebuilds and deploys automatically.

```bash
hugo new posts/my-new-post.md   # or just create the file by hand
```

## Local preview (optional)

The theme breaks on Hugo ≥ 0.123, so install Hugo **extended 0.111.3** specifically:

```bash
# macOS — download the pinned release rather than `brew install hugo` (brew gives latest)
curl -LO https://github.com/gohugoio/hugo/releases/download/v0.111.3/hugo_extended_0.111.3_darwin-universal.tar.gz
tar xzf hugo_extended_0.111.3_darwin-universal.tar.gz hugo && mv hugo /usr/local/bin/hugo-0.111

git submodule update --init --recursive   # fetch the theme (first time only)
hugo-0.111 server -D                      # http://localhost:1313
```

## Customizing

- `config.toml` — title, bio, menu, sidebar, sharing options. Theme docs: [user.md](https://github.com/kakawait/hugo-tranquilpeak-theme/blob/master/docs/user.md)
- `static/images/cover.jpg` — header cover image (placeholder included, replace with your own)
- `static/images/avatar.png` — profile picture (or set `gravatarEmail` in config.toml)
