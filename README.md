# harrisaman.github.io

My personal portfolio site. One self-contained HTML file — no build step, no
dependencies, no framework.

**Live at:** https://harrisaman.github.io

## Editing it

All the content lives in a config block near the top of the `<script>` tag in
`index.html`. Change those values and the page updates itself — you don't need to
touch any HTML or CSS.

| Object | Controls |
|---|---|
| `PROFILE` | Name, role, email, GitHub and LinkedIn links |
| `ABOUT` | The two "about" paragraphs |
| `SKILLS` | The skills grid (add or remove groups freely) |
| `PROJECTS` | Featured projects — cards, modals, run instructions, source code |
| `MORE_PROJECTS` | The smaller projects list, with embedded source |

### Adding a project

Append an object to `PROJECTS`. Only `title`, `tagline`, `tags`, `overview`,
`stack` and `highlights` are required. Optional extras:

- `github` / `demoUrl` — links. Left as `"#"`, the buttons are hidden rather
  than rendered as dead links.
- `tryIt` — the "Run locally" instructions block.
- `filename` + `code` — embeds the source in a scrollable viewer.

### Publishing a change

Edit `index.html`, then:

```bash
git add index.html
git commit -m "describe what changed"
git push
```

GitHub Pages redeploys within a minute or two.

## Files

- `index.html` — the entire site
- `.nojekyll` — tells GitHub Pages to serve files as-is rather than running them
  through Jekyll
