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

## Cloudflare Pages settings

Use these build settings:

- Production branch: `main`
- Build command: `exit 0`
- Build output directory: `public`

After the first deployment, Cloudflare gives the project a hostname ending in
`.pages.dev`.

## Connect the Square-managed domain without moving nameservers

1. In the Cloudflare Pages project, add `www.jumblestep.com` as a custom domain.
2. In Square, open the DNS records for `jumblestep.com`.
3. Add a CNAME record:
   - Host: `www`
   - Points to: the Cloudflare Pages hostname, such as `your-project.pages.dev`
4. In Square's domain destination settings, forward `jumblestep.com` to
   `https://www.jumblestep.com`.
5. Do not delete email MX or TXT records.

Use `https://www.jumblestep.com` as the public company website during the Apple
Developer membership conversion.

## Before publishing

Activate `hello@jumblestep.com`, or replace it everywhere in `public/index.html`
with another working address at the same domain.
