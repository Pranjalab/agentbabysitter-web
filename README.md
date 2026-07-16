# agentbabysitter-web

The landing page for **[Agent Babysitter](https://github.com/Pranjalab/AgentBabysitter)** — a
single, self-contained `index.html` (inline CSS, no build step, no dependencies).

## Preview locally

```sh
# any static server works; for example:
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser.

## Deploy

It's one static file, so it hosts anywhere — GitHub Pages, Vercel, Netlify, or the
`agentbabysitter.com` domain. For GitHub Pages, enable Pages on this repo (serve
from the default branch root) and, for the custom domain, add a `CNAME` file
containing `agentbabysitter.com`.

## License

MIT — see [LICENSE](LICENSE).
