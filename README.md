# 5740-final

Final project for STSCI 3/5740.

## Set-Up

### Prerequisites

- **R** (4.x): [https://cloud.r-project.org/](https://cloud.r-project.org/)
- **Quarto**: [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

After installing, confirm in a terminal:

```bash
R --version
quarto --version
pandoc --version
```

If `pandoc --version` fails, install Pandoc:

```bash
brew install pandoc
```

### Enter R from the terminal

1. Open Terminal (or the integrated terminal in Cursor).
2. Type `**R**` and press Enter.

You should see the R version and a `**>**` prompt. To quit R, type `q()`, press Enter. Choose whether or not to save workspace.

To run a single R command without opening an interactive session:

```bash
Rscript -e 'print(R.version.string)'
```

### R packages to install

Start R (see above), then run:

```r
install.packages(
  c("knitr", "rmarkdown", "tidyverse", "dplyr", "readr"),
  repos = "https://cloud.r-project.org"
)
```

Or from the shell without entering R:

```bash
Rscript -e 'install.packages(c("knitr", "rmarkdown", "tidyverse", "dplyr", "readr"), repos = "https://cloud.r-project.org")'
```

### Render the report

From the project root:

```bash
quarto render model.rmd
```

This produces `model.html` next to the source file.

### Open the HTML output

On macOS, from the project root:

```bash
open model.html
```

