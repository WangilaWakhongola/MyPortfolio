# Emmanuel W 

A personal portfolio website for Emmanuel W. Wakhongola, a Mathematics & Computer Science student building intelligent, secure, and user-friendly systems. The site features an interactive role-selector landing page (Recruiter, Developer, Client, Explorer) that tailors the experience for different visitors.

**Live site:** [https://wangilawakhongola.github.io/MyPortfolio/](https://wangilawakhongola.github.io/MyPortfolio/)

## Tech Stack

- Plain HTML, CSS, and vanilla JavaScript (no build step required)
- Hosted via GitHub Pages

## Running Locally

Because the site is a single static HTML file, you can preview it in any of the following ways:

```bash
# Option 1 — open directly in your browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option 2 — serve with Python (avoids some CORS quirks with local fonts)
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploying

The site is deployed automatically to **GitHub Pages** on every push to `main` via the workflow in `.github/workflows/static.yml`. No manual deployment step is needed.

To host your own fork:
1. Fork this repository.
2. Go to **Settings → Pages** and set the source to the `main` branch.
3. GitHub Pages will publish the site at `https://<your-username>.github.io/MyPortfolio/`.

## Contributing

Contributions, suggestions, and bug reports are welcome!

1. **Open an issue** to discuss the change you'd like to make before submitting a PR.
2. **Fork** the repository and create a feature branch (`git checkout -b feat/your-improvement`).
3. Make your changes and verify the site still looks correct locally.
4. **Open a Pull Request** against the `main` branch with a clear description of what changed and why.

Please keep PRs focused and minimal — one logical change per PR makes review easier.

## License

This project is open source. Feel free to use the code as inspiration for your own portfolio.
