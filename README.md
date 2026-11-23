# Connected — A Moment Between Moments (website POC)

A dependency-free static website with a central landing page and six deep-linkable worksheets.

## Run locally

Open `index.html` in a browser, or serve this folder with:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy

Upload the contents of this folder (index.html, styles.css, app.js) to a static hosting service such as Netlify Drop, GitHub Pages, Cloudflare Pages, or Vercel. No build step, API key, database, or server-side code is required. Ensure all three files remain together.

## Individual worksheet links

Append these paths to your website's base URL:

- `?worksheet=danny-school` — Danny: School-morning rush
- `?worksheet=amos-growth` — Amos: Sleeping independently
- `?worksheet=amos-fairness` — Amos: Playground dispute
- `?worksheet=danny-voice` — Danny: YouTube incident
- `?worksheet=jeeb-childhood` — Jeeb: School event
- `?worksheet=jeeb-curiosity` — Jeeb: Someone at the window

The home page links to all six.

## Features

- Two-level worksheets with original guided response prompts
- Automatic browser-local draft saving (localStorage)
- Preview and selectively include responses on card
- Download a PNG card, use native share where available, or copy text
- Responsive mobile layout
- No tracking, backend storage, or publication of answers

## Limitations / next steps

- Video placeholders need to be replaced with the final Shoot 3 video embeds or links.
- Cards use system fonts, not official Connected brand assets.
- Data is saved only on the same browser/device; clearing browser storage removes drafts. This is not a durable account-based archive.
- Community bulletin board, admin analytics, and participant feedback collection are not included.
- Native image sharing varies by browser and device; PNG download is the fallback.
- For formal user research, add consent, privacy notice, and separately configured feedback capture before collecting personal responses.

## Editing content

The six worksheets and their questions are in the `TOPICS` array near the top of `app.js`.

## Deploy to Vercel

The included `vercel.json` configures this as a static site with no build command.

**Recommended dashboard workflow:** Create a new GitHub repository, upload the files from this folder to the repository root, then choose **Add New > Project** in Vercel, import the repository, select **Other** as framework if prompted, and deploy. Leave build command blank and output directory at the project root.

**Alternative CLI workflow:** Install the Vercel CLI (`npm i -g vercel`), open a terminal in this folder, run `vercel login` and then `vercel --prod`. Follow the interactive prompts. A Vercel account and internet access are required.

Vercel's dashboard generally imports Git repositories rather than accepting a ZIP as a direct upload. The ZIP is provided as a convenient way to obtain all the files together.
