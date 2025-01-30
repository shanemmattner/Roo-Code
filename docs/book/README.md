# Jupyter Book Documentation

This repository includes a Jupyter Book that is automatically built and deployed to GitHub Pages.

## Initial Setup

1. Clone the repository with submodules:
   ```bash
   git clone --recursive https://github.com/shanemmattner/Roo-Code.git
   cd Roo-Code
   ```

2. Set up the Jupyter Book environment:
   ```bash
   cd submodules/jupyter-book-assistant
   python3 -m venv venv
   source venv/bin/activate
   pip install ghp-import
   ./setup_submodule.sh
   ```

## Making Updates to the Book

1. The book content is located in `docs/book/`. You can:
   - Edit existing markdown files (`.md`)
   - Add new markdown files or Jupyter notebooks (`.ipynb`)
   - Update `_toc.yml` to include new files in the table of contents
   - Customize `_config.yml` for book settings

2. Build the book locally to preview changes:
   ```bash
   cd submodules/jupyter-book-assistant
   source venv/bin/activate
   ./generate_book.sh
   ```

3. View your changes by opening `docs/book/_build/html/index.html` in your browser

## Publishing Changes

When you're ready to publish your changes:

1. Activate the virtual environment and run the generate script:
   ```bash
   cd submodules/jupyter-book-assistant
   source venv/bin/activate
   ./generate_book.sh
   ```

2. The script will:
   - Build the book
   - Create or update the gh-pages branch
   - Deploy to GitHub Pages

Your book will be available at: https://shanemmattner.github.io/Roo-Code/

## Book Structure

```
docs/book/
├── _config.yml        # Book configuration
├── _toc.yml          # Table of contents
├── intro.md          # Landing page
├── markdown.md       # Example markdown file
└── notebooks.ipynb   # Example notebook
```

## Troubleshooting

1. **Missing ghp-import?**
   ```bash
   source venv/bin/activate
   pip install ghp-import
   ```

2. **Build errors?**
   - Check the build logs in the terminal
   - Ensure all required files are properly referenced in `_toc.yml`
   - Verify any Jupyter notebooks can execute successfully

3. **Book not updating?**
   - Make sure you're in the virtual environment (`source venv/bin/activate`)
   - Run `./generate_book.sh` to rebuild and deploy
   - Changes should appear on the website within a few minutes

## Need Help?

- [Jupyter Book Documentation](https://jupyterbook.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- Open an issue in this repository for specific problems