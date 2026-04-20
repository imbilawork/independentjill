# Independent Jill — Website

Single-page site for Jill Murtagh. No CMS, no build step — just `index.html` plus two images in `assets/`. Edits are made by opening the file (or asking Claude Code to change a line).

## Files
- `index.html` — the whole site
- `assets/IJ_logo.png` — brand logo (nav + footer + favicon)
- `assets/JillPic.jpg` — hero portrait

## Local preview
```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Contact form — one-time setup
The form uses [FormSubmit](https://formsubmit.co) (free, no account). To activate:

1. In `index.html`, find `YOUR_EMAIL_HERE` and replace with Jill's email address:
   ```html
   <form ... action="https://formsubmit.co/ajax/jill@example.com" ...>
   ```
2. Submit the form once from the live site. FormSubmit emails a confirmation link — click it to activate.
3. From then on, every enquiry lands in Jill's inbox.

Until step 1 is done, the form shows a friendly "not yet connected" message and asks visitors to call/email directly.

## Making small edits
Common changes Jill can ask Claude Code to make:
- Update copy in hero / about / services sections
- Change phone number or add email address
- Add a new service card
- Swap the portrait photo (drop new image into `assets/` and update `src="assets/..."`)
- Tweak colours — all brand tokens are defined at the top of the `<style>` block (`--purple-*`, `--gold-*`)

## Deploying
Works on any static host:
- **Cloudflare Pages** — drag-drop the folder at dash.cloudflare.com/pages
- **Netlify** — drag-drop the folder at app.netlify.com/drop
- **GitHub Pages** — push the folder to a repo, enable Pages in settings
