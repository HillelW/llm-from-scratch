# llm-from-scratch

This repository contains a notebook-first course on building language models from the ground up.

The committed project surface is intentionally small.

The `notebooks/` directory contains the chapter notebooks, and the rest of the repo is kept minimal so the learning path stays focused.

## Setup

Install `uv`, then create the locked development environment.

```sh
uv sync --locked --dev
```

## Chapters

- [Chapter 1](notebooks/chapter-01-what-we-are-actually-building.ipynb)
- [Chapter 2](notebooks/chapter-02-from-text-to-training-examples-and-generation.ipynb)
- [Chapter 3](notebooks/chapter-03-clear-notebooks-visible-data-and-no-magic.ipynb)
- [Chapter 4](notebooks/chapter-04-text-as-data-strings-characters-and-finite-sequences.ipynb)
- [Chapter 5](notebooks/chapter-05-reading-text-files-and-inspecting-a-corpus.ipynb)
- [Chapter 6](notebooks/chapter-06-cleaning-text-without-over-cleaning.ipynb)
- [Chapter 7](notebooks/chapter-07-character-level-tokenization.ipynb)
