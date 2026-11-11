# ReelJesus

A static blog with custom HTML and CSS. GitHub Pages builds the site with Jekyll. Pages CMS provides a browser editor for writing posts and uploading images.

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
