# Jupyter Book Documentation

This repository includes a Jupyter Book that is automatically built and deployed to GitHub Pages.

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/shanemmattner/Roo-Code.git
   cd Roo-Code
   ```

2. Add or modify content in the `docs/book` directory:
   - Edit existing markdown files (`.md`)
   - Add new markdown files or Jupyter notebooks (`.ipynb`)
   - Update `_toc.yml` to include new files in the table of contents
   - Customize `_config.yml` for book settings

3. Push your changes:
   ```bash
   git add .
   git commit -m "Update book content"
   git push
   ```

That's it! The GitHub Actions workflow will automatically:
- Build your Jupyter Book
- Deploy it to GitHub Pages
- Make it available at: https://shanemmattner.github.io/Roo-Code/

## Book Structure

```
docs/book/
├── _config.yml        # Book configuration
├── _toc.yml          # Table of contents
├── intro.md          # Landing page
├── markdown.md       # Example markdown file
└── notebooks.ipynb   # Example notebook
```

## Local Development

If you want to preview changes locally before pushing:

1. Install dependencies:
   ```bash
   pip install -r docs/book/requirements.txt
   ```

2. Build the book:
   ```bash
   cd docs/book
   jupyter-book build .
   ```

3. Open `_build/html/index.html` in your browser to preview.

## Troubleshooting

1. **Book not updating?**
   - Check the Actions tab in GitHub to see if the workflow ran successfully
   - Ensure your changes are in the `main` branch
   - Try triggering the workflow manually from the Actions tab

2. **Build errors?**
   - Check the build logs in GitHub Actions
   - Try building locally to debug issues
   - Ensure all required files are properly referenced in `_toc.yml`

## Need Help?

- [Jupyter Book Documentation](https://jupyterbook.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- Open an issue in this repository for specific problems