# ReelJesus

A static blog with custom HTML and CSS. GitHub Pages builds the site with Jekyll. Pages CMS provides a browser editor for writing posts and uploading images.

## 1. Put the files on GitHub

1. Unzip the starter.
2. At https://github.com/new, create a **public** repository named `reeljesus`. Add a README when creating it to initialize the `main` branch.
3. In the repo, use **Add file → Upload files**. Drag in the **contents** of the extracted folder, keeping `_layouts`, `_posts`, and `assets` intact. Commit to `main`.
4. Verify that `index.html`, `_config.yml`, and `.pages.yml` sit at the repository root. On a Mac, press **Command + Shift + .** in Finder to show dotfiles. If the upload missed `.pages.yml`, create that exact filename through **Add file → Create new file**, paste in the configuration from the ZIP, and commit it.

If using a cloned repository instead, copy the same files into its root, then commit and push to `main`.

## 2. Enable the public site

1. In the repository, open **Settings → Pages**.
2. Choose **Deploy from a branch → main → /(root)** and save.
3. Return to **Settings → Pages → Visit site** after deployment. With the suggested repository name, the address will look like `https://YOUR-USERNAME.github.io/reeljesus/`.
4. Open the sample post. Its cover and its inline illustration should both load. Keep Jekyll enabled because it renders the post templates and feed. Opening the source HTML directly in Finder will show template tags.

## 3. Connect the browser editor

1. Open https://app.pagescms.org/ and sign in with GitHub.
2. Install Pages CMS on the account that owns the repository. When GitHub asks for repository access, select **Only select repositories** and choose your blog repository.
3. Open your blog repository and select `main` in Pages CMS. The supplied `.pages.yml` should give you a **Posts** collection.
4. Open the sample entry and make a small edit. Save, confirm the commit appears on `main`, and check the live page after the next deployment finishes.

## 4. Publish a post with pictures

1. In Pages CMS, open **Posts** and create an entry.
2. Enter a title, a post date, and an optional summary. For a post that should go live immediately, use today’s date or an earlier one.
3. For a cover, click **Cover image** and upload or select a picture. Describe it in **Cover image description**.
4. Write in **Post body**. To insert a picture between paragraphs, use the image control in the rich-text toolbar. Add descriptive alt text in the image controls or in Source mode if needed.
5. Save. The editor writes the post and uploads to GitHub. Check the repo’s **Actions** tab for the Pages build and open the live site when it finishes.

The public blog and the editor are separate. Only authorized GitHub users can edit through Pages CMS. A public repo exposes committed content, so keep private drafts outside it until you are ready to publish.

## Files and customization

| File or directory | Purpose |
| --- | --- |
| `index.html` | Homepage and latest-post feed |
| `_layouts/default.html` | Shared header, footer, and document structure |
| `_layouts/post.html` | Reusable post layout, including cover and inline image paths |
| `assets/style.css` | Colors, fonts, and responsive layout |
| `_config.yml` | Blog name, description, author, and Jekyll settings |
| `.pages.yml` | Browser editor fields and upload configuration |
| `_posts/` | Posts written as Markdown with metadata |
| `assets/uploads/` | Cover and inline images |

Change the title, tagline, or author in `_config.yml`. To use your own design, edit the homepage and layouts while keeping the Liquid post loop, the post body placeholder, and the `relative_url` filters. The sample welcome post is editable from Pages CMS.

## Troubleshooting

- **Pages CMS asks for a configuration:** Check that `.pages.yml` is in the root of `main`.
- **A post is missing:** Check the Pages build in GitHub Actions, confirm the date is not in the future, and confirm that the post is under `_posts` with a filename beginning `YYYY-MM-DD-`.
- **A picture is missing:** Confirm the image exists under `assets/uploads/` and the filename matches. Use the editor’s image controls to create a path the templates recognize.
