# Family Heritage Website: setup guide

A simple Jekyll site that GitHub Pages builds automatically. There's no software to install. You can edit everything in the browser on github.com.

## IMPORTANT: privacy first

A site on **GitHub Pages is public**: anyone with the link can see it, even if the repository is private.
Until a private, family-only section is set up, only upload:
- old or heritage photos (grandparents, ancestors, places, festivals)
- stories about people who have passed away

Keep photos of living family (especially children), full birth dates and addresses off the site for now.

## 1. Create the site (about 10 minutes)

1. Sign in at https://github.com (create a free account if needed).
   Choose your username carefully: the site address will be `https://USERNAME.github.io/REPO-NAME/`.
2. Click **+** (top right) → **New repository**.
   - Name: `family` (or similar)
   - Visibility: **Public** (free accounts need this for Pages)
   - Click **Create repository**.
3. On the new repo page, click **uploading an existing file**.
   Unzip `family-site.zip` on your computer, open the folder, select **everything inside it**
   (including the `_layouts`, `_people` and `assets` folders) and drag it into the browser.
   Click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, choose
   Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)** → **Save**.
5. Wait 1–2 minutes, refresh the Pages settings, and click the link shown. Your site is live.

## 2. Add photos

1. **Resize first**: phone photos are 3–8 MB; aim for ~1600 px wide (about 300–500 KB).
   On Windows: open in Photos → "…" → Resize image. On Mac: Preview → Tools → Adjust Size.
2. Name them descriptively: `1972-grandmother-diwali.jpg` (the name becomes the caption).
3. In the repo, open `assets/photos` → **Add file → Upload files** → drag photos in → **Commit**.
4. They appear on the Gallery page automatically after a minute.

## 3. Add a person

1. Open the `_people` folder, click a file (e.g. `great-grandfather.md`), then the copy icon to copy its text.
2. In `_people`, click **Add file → Create new file**, name it like `grandmother-name.md`, paste, edit, **Commit**.
3. `generation` controls the ordering on the People page (1 = oldest).
4. To show a portrait, upload the photo to `assets/photos` and set `photo: /assets/photos/her-photo.jpg`
   (remove the `#` at the start of that line).

## 4. Edit text pages

`index.md` (home), `origins.md`, `traditions.md` are plain text in Markdown.
Click the file → pencil icon → edit → **Commit changes**.

## Folder layout

```
_config.yml        site title and settings
index.md           home page
people.md          list of everyone (automatic)
_people/           one file per family member
origins.md         where the family comes from
traditions.md      festivals, faith, food, customs
gallery.md         photo gallery (automatic)
assets/photos/     all photos go here
assets/css/        styling
_layouts/          page templates (rarely need changing)
```

## Later steps

- Custom domain (e.g. ourfamily.com), prepaid for 10 years: Settings → Pages → Custom domain
- Private family-only section (Cloudflare Pages + Cloudflare Access)
- Download a backup zip regularly: Code → Download ZIP
