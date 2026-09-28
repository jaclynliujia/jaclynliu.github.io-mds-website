# jaclynliu.github.io-mds-website
MDS Website
# DSCI 521 Data Science Website

This repository contains my Quarto website for DSCI 521. It includes computational posts written in both Python and R.

## Requirements

Install the following before building the website:

- Quarto
- uv
- Python 3.14
- R 4.6.1
- Git

Python dependencies are managed with `uv`, and R dependencies are managed with `renv`.

## Build instructions

### 1. Clone the repository

```bash
git clone git@github.com:jaclynliujia/jaclynliu.github.io-mds-website.git
cd jaclynliu.github.io-mds-website
```

### 2. Restore the Python environment

From the top level of the repository:

```bash
uv sync
```

### 3. Restore the R environment

From the top level of the repository:

```bash
Rscript -e 'renv::restore(prompt = FALSE)'
```

### 4. Render the website

From the top level of the repository:

```bash
uv run quarto render
```

The rendered website is written to the `docs/` directory.

### 5. Preview the built website

To preview the website locally:

```bash
uv run quarto preview
```

## Data sources

The Python computational post uses the Iris dataset distributed with `scikit-learn`.

The R computational post uses the `mtcars` dataset included with R.

Both datasets are provided through the installed Python or R environments, so no separate data files need to be downloaded at render time.