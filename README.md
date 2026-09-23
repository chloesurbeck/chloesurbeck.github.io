# chloesurbeck.github.io

This repository hosts my data science portfolio while at UBC. It contains a landing/about page, a relevant blog and two computing environments.

- **Live Website**: <https://chloesurbeck.github.io>
- **GitHub Repository**: <https://github.com/chloesurbeck/chloesurbeck.github.io>

## 1. Required Tools

Before building the site, ensure you have the following software installed on your system:

- [**Git**](https://git-scm.com/) (version 2.40+)
- [**Quarto CLI**](https://quarto.org/docs/get-started/) (version 1.5+)
- [**uv**](https://docs.astral.sh/uv/) (Python package and environment manager, version 0.4+)
- [**R**](https://cloud.r-project.org/) (version 4.4+)

## 2. Build Instructions

Follow the steps in order from a terminal (bash) to clone the repository, restore both computing environments and render the complete website.

### Step 1: Clone the Repository

Run in your shell:

``` bash
git clone https://github.com/chloesurbeck/chloesurbeck.github.io.git
cd chloesurbeck.github.io
```

(renv does not need to be manually pre-installed; it bootstraps itself via .Rprofile)

### Step 2: Restore the Python Environment

Run in your shell from the repository root:

``` bash
uv sync
```

### Step 3: Restore the R Environment

Run in your shell from the repository root:

``` bash
Rscript -e "renv::restore()"
```

### Step 4: Render the Website

Run in your shell from the repository root:

``` bash
uv run quarto render
```

## 3. Site Landing & Local Opening

- **Output Location**: Quarto renders into the **`docs/`** directory (which is published to GitHub).
- **Opening Site Locally**:
  - Run in your shell from the repository root:

    ``` bash
    uv run quarto preview
    ```

## 4. Data Source & Network Requirements

- **Data Source**: Palmer Archipelago penguin data from the `palmerpenguins` library. ([Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/), Palmer Station Antarctica LTER)
- **Network Requirements**: None; all data is bundled within the installed `palmerpenguins` packages for Python and R