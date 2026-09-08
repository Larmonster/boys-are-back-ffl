# Boys Are Back HQ

Source for the league site for **The Boys Are Back** fantasy football league —
weekly fight cards, standings, and an archive, all on one page (`index.html`).

## Push this to GitHub

```bash
gh repo create boys-are-back-ffl --public --source=. --remote=origin --push
```

Or manually:

```bash
git remote add origin https://github.com/<your-username>/boys-are-back-ffl.git
git branch -M main
git push -u origin main
```

## Host it for free with GitHub Pages

After pushing: repo **Settings → Pages → Deploy from a branch → main / (root)**.
Your league gets a permanent link like `https://<your-username>.github.io/boys-are-back-ffl/`.

## Updating week to week

Everything lives in the `WEEKS` array near the top of the `<script>` tag in
`index.html`. Add a new object to that array each week (copy the Week 1 block
as a template) and the Home tab, This Week tab, Standings, and Archive all
render from it automatically — fill in `score` once games go final and a
week's `status` to `"final"` to have it count toward Standings.
