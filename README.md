# llm-from-scratch

This repository contains a notebook-first course on building language models from the ground up.

The chapters are in the [`notebooks/`](notebooks/) directory and are intended to be run in order.

Everything runs on CPU; a GPU and CUDA are not required.

## Prerequisites

Install these tools before cloning the repository:

- [Git](https://git-scm.com/downloads)
- [uv](https://docs.astral.sh/uv/getting-started/installation/)

The project uses Python 3.11.

`uv` reads the included `.python-version` file and installs the appropriate Python version if needed.

## Clone and install

Run these commands in a terminal:

```sh
git clone https://github.com/HillelW/llm-from-scratch.git
cd llm-from-scratch
uv sync --locked --dev
```

The final command creates a local `.venv` and installs the exact dependencies recorded in `uv.lock`.

## Open the notebooks

From the repository root, start JupyterLab through the project environment:

```sh
uv run jupyter lab
```

JupyterLab will print a local URL and normally open it in your browser automatically.

In JupyterLab, open the `notebooks/` directory and select a chapter, such as `chapter-01-what-we-are-actually-building.ipynb`.

Run cells with `Shift+Enter`, or use **Run > Run All Cells** to execute the entire notebook.

When finished, return to the terminal and press `Ctrl+C` to stop JupyterLab.

Always launch JupyterLab with `uv run` from the repository root.

This ensures the notebooks use the project's Python version and installed packages rather than a system-wide Jupyter installation.

## Run a notebook from the terminal

To execute a notebook without opening the browser, run:

```sh
uv run jupyter nbconvert \
  --to notebook \
  --execute \
  --inplace \
  --ExecutePreprocessor.timeout=300 \
  notebooks/chapter-01-what-we-are-actually-building.ipynb
```

The `--inplace` option saves the generated outputs back into that notebook.

Replace the final path to run a different chapter.

## Troubleshooting

If imports fail or Jupyter uses the wrong Python environment, stop JupyterLab and run these commands again from the repository root:

```sh
uv sync --locked --dev
uv run jupyter lab
```

You can confirm the active Python and PyTorch versions with:

```sh
uv run python -c "import sys, torch; print(sys.version); print(torch.__version__)"
```
