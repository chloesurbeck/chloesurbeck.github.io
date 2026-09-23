# chloesurbeck.github.io

This repository hosts the source code and rendered artifacts for Chloe Surbeck's personal academic portfolio and data science blog, built with [Quarto](https://quarto.org/).

- **Live Website**: [https://chloesurbeck.github.io](https://chloesurbeck.github.io)
- **GitHub Repository**: [https://github.com/chloesurbeck/chloesurbeck.github.io](https://github.com/chloesurbeck/chloesurbeck.github.io)

---

## Prerequisites

Before building the site, ensure you have the following tools installed on your system:

1. **[Git](https://git-scm.com/)**
2. **[Quarto CLI](https://quarto.org/docs/get-started/)** (version 1.5 or newer)
3. **[uv](https://docs.astral.sh/uv/)** (Fast Python package and project manager)
4. **[R](https://cloud.r-project.org/)** (version 4.4 or newer)

---

## Reproduction & Build Instructions

Follow the steps below to clone the repository, restore the Python and R computing environments, and render the complete website.

### 1. Clone the Repository

```bash
git clone https://github.com/chloesurbeck/chloesurbeck.github.io.git
cd chloesurbeck.github.io
```

### 2. Set Up the Python Environment

The Python environment is managed using `uv` (configured in `pyproject.toml` and pinned in `uv.lock`). Run:

```bash
uv sync
```

This will automatically create a virtual environment (`.venv/`) and install all required packages (including `jupyter`, `pandas`, `matplotlib`, and `palmerpenguins`).

### 3. Set Up the R Environment

The R environment is managed using `renv` (configured via `.Rprofile` and pinned in `renv.lock`). Run:

```bash
Rscript -e "renv::restore()"
```

This will install all necessary R packages (including `palmerpenguins`, `dplyr`, `tidyr`, `ggplot2`, and `rmarkdown`) into the project's local library.

### 4. Render the Website

Once both environments are restored, render the complete site into the `docs/` folder:

```bash
uv run quarto render
```

### 5. Preview Locally (Optional)

To start a local live-reloading development server to view the site in your browser:

```bash
uv run quarto preview
```

---

## Project Structure

```text
chloesurbeck.github.io/
├── _quarto.yml             # Quarto site configuration
├── index.qmd               # Home landing page
├── about.qmd               # About page
├── blog.qmd                # Blog listing page
├── posts/
│   ├── first-weeks/        # Reflection on first weeks in MDS
│   ├── python-penguins/    # Palmer Penguins data analysis in Python
│   └── r-penguins/         # Palmer Penguins data analysis in R
├── docs/                   # Rendered static site deployed to GitHub Pages
├── pyproject.toml          # Python project & dependency specifications
├── uv.lock                 # Pinned Python lockfile
├── .Rprofile               # renv project auto-activation script
└── renv.lock               # Pinned R lockfile
```