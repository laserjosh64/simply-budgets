# Simply Budgets on GitHub

Set up the same way as Stackbound: a public repository on the `laserjosh64` account, served by GitHub Pages, with Claude pushing each build.

- **Repository:** https://github.com/laserjosh64/simply-budgets (public)
- **Website:** https://laserjosh64.github.io/simply-budgets/
- **Hosting:** GitHub Pages, free, from the `main` branch, root folder

## One-time setup (your part)

1. **Make the repository.** On GitHub, tap **+**, then **New repository**. Name it `simply-budgets`, leave it **Public**, and don't add any files.
2. **Let Claude in.** Go to https://github.com/apps/claude/installations/select_target, pick `laserjosh64`, and add `simply-budgets` under **Repository access**.
3. **Add it to a Claude project.** In the project where you'll work on the app, add `laserjosh64/simply-budgets` under Project settings, Resources. Start a chat in that project, attach `simply-budgets.zip`, and ask Claude to push it.
4. **Switch on the website** after the first push. In the repository, open **Settings**, then **Pages**. Set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, and tap **Save**. Claude can't change Pages settings, so this step is yours.
5. **Install it.** Open the website in Safari, tap **Share**, then **Add to Home Screen**. On Android, use Chrome's menu and pick **Install app**. Open it once with signal so it saves itself for offline use.

## What Claude does for each update

```bash
cd simply-budgets-site
git pull origin main
find . -mindepth 1 -maxdepth 1 ! -name .git -exec rm -rf {} +   # clear the old build
cp -r ../simply-budgets/. .                                  # drop in the new build
python3 tools/make_sw.py                                     # new version from the file contents
git add -A
git commit -m "Short description of the change"
git push origin main
```

GitHub rebuilds the site within a minute or two. The **Actions** tab shows a "pages build and deployment" run that turns green when it's live.

## Things to know

- **Phones update themselves.** The installed app checks for a new build whenever it's opened and shows an Update button when one is ready. Tapping it reloads into the new version. Saved data stays.
- **Always ship a fresh `sw.js`.** If a file is changed by hand, run `tools/make_sw.py` before uploading. Without it, installed phones keep the old version.
- **Each copy has its own data.** The home screen app, the website in the browser, and the claude.ai preview each keep separate saves.
- **The repository is public.** Anyone can read the code. Nobody's budget data is in it; that stays on each phone.
- **A 404 page** means Pages isn't on yet, GitHub is still publishing, or the files went into a subfolder instead of the top level.
