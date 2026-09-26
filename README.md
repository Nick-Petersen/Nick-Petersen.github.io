# Nick Petersen's Personal Website

This repository contains my personal website created using Quarto. It includes computational blog posts written in both Python and R.

## Requirements

The following software is required to reproduce the website. The versions used to build this site were:

- Quarto 1.10.18
- uv 0.12.7
- R 4.6.1

The Python environment is managed using `uv`, and the R environment is managed using `renv`.

## Build Instructions

Clone the repository and move into the project directory:

```bash
git clone git@github.com:Nick-Petersen/Nick-Petersen.github.io.git
cd Nick-Petersen.github.io
```

Set up the Python environment from the `uv.lock` file:

```bash
uv sync
```

Restore the R environment by starting R from the top level of the repository:

```bash
R
```

Then, in the R console, run:

```r
renv::restore()
```

Exit R:

```r
q()
```

Then render the website from the top level of the repository:

```bash
uv run quarto render
```

The rendered website is written to the `docs/` directory.

To preview the website locally, run:

```bash
uv run quarto preview
```

## Data

The Python and R computational posts use the Palmer Penguins dataset from Palmer Station Antarctica LTER:

https://allisonhorst.github.io/palmerpenguins/

The dataset is provided through the `palmerpenguins` packages used by the project environments, so the dataset does not need to be downloaded separately at render time.