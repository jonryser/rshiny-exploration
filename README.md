# rshiny-exploration

Exploring Rshiny

## Requirements

Install:

- R: [https://www.r-project.org/](https://www.r-project.org/)

- RStudio: [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/)

## Local Shiny-iAtlas Session

To run the app locally:

1. Clone this repository

1. Start Rstudio

1. Create a "New Project..." from the "File" menu

1. Create a project from an "Existing Directory"

1. Navigate to the cloned project folder.

1. Select the project folder.

1. In the "console" tab in Rstudio, a new R session will start. This will execute `source("renv/activate.R")` from the `.Rprofile.d/default.R` file and `renv` will bootstrap itself in.

1. At the prompt in the "console" tab, restore the dependecies by running:

   ```R
   renv::restore()
   ```

   This may take some time to complete - get something nice to drink :)

1. Start the app by running:

   ```R
   shiny::runApp()
   ```

## Development

When adding any new dependencies to the application, they may be added using:

```R
renv::install()
```

see [https://rstudio.github.io/renv/reference/install.html](https://rstudio.github.io/renv/reference/install.html) for more details.

Once a new package is added, run:

```R
renv::snapshot()
```

This will ensure the new package is added to the renv.lock file.

For more on package management with renv, please see [https://rstudio.github.io/renv/articles/renv.html](https://rstudio.github.io/renv/articles/renv.html)
