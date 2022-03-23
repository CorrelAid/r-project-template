Project name
================

# What is this project about?

summarize in three sentences what this project is about and what central
features it has.

# Setup

## Installing Packages

`renv` brings project-local R dependency management to our project.
`renv` uses a lockfile (`renv.lock`) to capture the state of your
library at some point in time. Based on `renv.lock`, RStudio should
automatically recognize that it’s being needed, thereby downloading and
installing the appropriate version of `renv` into the project library.
After this has completed, you can then use `renv::restore()` to restore
the project library locally on your machine. When new packages are used,
`install.packages()` does not install packages globally, it does in an
environment only used for our project. You can find this library in
`renv/library`. If `renv` fails, you will be presented something in the
like of when you first start R after cloning the repo:

    renv::restore()
    This project has not yet been activated. Activating this project will ensure the project library is used during restore. Please see ?renv::activate for more details. Would you like to activate this project before restore? [Y/n]:

Follow along with `Y` and `renv::restore()` will do its work downloading
and installing all dependencies. `renv` uses a local `.Rprofile` and
`renv/activate.R` script to handle our project dependencies. If a
developer adds a new package to a project, `renv::snapshot` updates the
lockfile which triggers an update cascade, once checked-in.

## Data

You need the following data files in order to run this project:

``` r
system2("tree", c("data/raw")) # works on mac and potentially linux. 
```

# Developer information

\[the following can also be moved to the wiki if you decide to have
one\]

## Definition of Done

## Code styling

# How to operate this project?

\[the following can also be moved to the wiki if you decide to have
one\]

explain how the output(s) of this project can be handled/operated, for
example:

-   how to knit the report(s)
-   where to create/find the data visualizations
-   how to update data
-   what would need to be updated if someone wanted to re-run your
    analysis with different data

# Limitations

be honest about the limitations of your project, e.g.:

-   methodological: maybe another model would be more suitable?
-   reproducibility: what are limits of reproducibility? is there
    something hard-coded/specific to the data that you used?
