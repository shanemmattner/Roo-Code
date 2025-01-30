# Roo Code

## Jupyter Book Documentation

This repository includes a Jupyter Book that is published at [https://shanemmattner.github.io/Roo-Code/](https://shanemmattner.github.io/Roo-Code/).

For detailed instructions on setting up and updating the book, see [docs/book/README.md](docs/book/README.md).

Quick start:
```bash
# Clone with submodules
git clone --recursive https://github.com/shanemmattner/Roo-Code.git
cd Roo-Code

# Set up Jupyter Book
cd submodules/jupyter-book-assistant
python3 -m venv venv
source venv/bin/activate
pip install ghp-import
./setup_submodule.sh

# Generate and publish the book
./generate_book.sh
```

The book will be available at https://shanemmattner.github.io/Roo-Code/

## Making Book Updates

1. Edit content in `docs/book/`
2. Run:
```bash
cd submodules/jupyter-book-assistant
source venv/bin/activate
./generate_book.sh
```

See [docs/book/README.md](docs/book/README.md) for more details on book management.
