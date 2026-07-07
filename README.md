# Bible Heads Up — Privacy Policy site

Static one-page privacy policy for the **Bible Heads Up** Android app, hosted on GitHub Pages
so Google Play has a public privacy-policy URL.

- **Live URL:** https://churchsoundlab.github.io/bible-heads-up-privacy/
- **Source of record:** the app repo's `PRIVACY.md` — keep `index.html` here in sync with it.

This folder is its **own** public git repo, separate from the private app repo (which
git-ignores `privacy/`). `.nojekyll` is present so GitHub Pages serves `index.html` as-is.

## First-time publish
```powershell
# inside bible-game-headsup/privacy
git init -b main; git add -A; git commit -m "Privacy policy site for Bible Heads Up"
gh repo create churchsoundlab/bible-heads-up-privacy --public --source=. --remote=origin --push
gh api --method POST repos/churchsoundlab/bible-heads-up-privacy/pages -f "source[branch]=main" -f "source[path]=/"
# live at https://churchsoundlab.github.io/bible-heads-up-privacy/ (first build takes a couple of minutes)
```
