# howardzijiesong.github.io

## Introduction

This is a Quarto website with two posts analysing a camera sensor dataset from: <https://github.com/openMVG/CameraSensorSizeDatabase>

There is a Python and R version.

## Tools to Install

- Quarto 1.10.18
- uv 0.12.12
- R 4.6.1

> If you are on Linux a C/C++ compiler will also be needed

## How to Build

### Step 1: Clone the repository

*Shell*

```bash
git clone https://github.com/howardzijiesong/howardzijiesong.github.io.git
cd howardzijiesong.github.io
```

### Step 2: Setup your Environment

*Shell*

```bash
uv sync
Rscript -e "renv::restore(prompt = FALSE)"
```

### Step 3: Render the project

*Shell*

```bash
uv run quarto render
```

### Step 4: Run the Python web server

*Shell*

```bash
uv run python -m http.server --directory docs 8000
```

Now open <http://localhost:8000> to view.

---


## Addenda

The site is built into the docs/ folder.

The build requires a network connection to download packages through uv and renv. The CSV is committed to the repository, so the data itself needs no network.

Viewing the posts requires an internet connection for one image, which is loaded from an external website.

If port 8000 is busy use another port number above 1024