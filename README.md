# Engineering portfolio

A static portfolio for GitHub Pages. All content lives in `data.json`, and photos live in an `images/` folder.

## Publish it

1. On GitHub, create a new public repository. Name it `YOUR-USERNAME.github.io` to get the address `https://YOUR-USERNAME.github.io`, or use any name to get `https://YOUR-USERNAME.github.io/REPO-NAME`.
2. Choose **Add file → Upload files**. Drag in `index.html`, `data.json`, and a folder named `images` that holds your photos. Commit.
3. Open **Settings → Pages**. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save. The site is live in about a minute.

## Edit your content

- Open `data.json` on GitHub, click the pencil icon, change the text, and commit. The site updates in a minute or so.
- Keep the quotes and commas as they are. If the page says it can’t load, a comma or quote is usually missing; paste the file into jsonlint.com to find it.
- Each project has `objective`, `approach`, `results`, `tags`, `tools`, and `specs` (label: value pairs). Projects appear in the order they are listed, so move a block up to move it to the top.
- To add a project, copy one block, give it a new unique `id`, and add a comma between blocks.

## Add photos

1. Upload the image into the `images` folder (JPG, about 1600 px wide, lowercase names with no spaces, such as `rocket-fin-can.jpg`).
2. Add its path to that project’s `photos` list. A caption is optional:

```json
"photos": [
  "images/rocket-fin-can.jpg",
  { "src": "images/rocket-test.jpg", "caption": "Static fire test" }
]
```

## Preview on your computer

Opening `index.html` directly won’t load `data.json`. From this folder, run `python3 -m http.server` and visit http://localhost:8000.
