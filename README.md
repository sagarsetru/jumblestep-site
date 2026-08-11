# Jumblestep website

A tiny, database-free company website for Jumblestep LLC.

## Edit the text

Open `public/index.html`. The two most important editable areas are marked with
`EDIT` comments. The rest of the page is ordinary HTML and CSS in one file.

## Preview locally

From this repository's root:

```bash
python3 -m http.server 8000 --directory public
```

Then open `http://localhost:8000` in a browser.

## Commit and push

```bash
git add .
git commit -m "Update Jumblestep website"
git push
```

When this repository is connected to Cloudflare Pages, every push to `main`
will deploy automatically.