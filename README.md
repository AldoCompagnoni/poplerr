
<!-- README.md is generated from README.Rmd. Please edit that file -->
Updates included in this version

-   Updated Roxygen documentation to include all dependencies and updated NAMESPACE accordingly

-   Updated some documentation so that it is more clear and/or CRAN compliant

-   updated `alt icon` folder name to `alt_icon` to make it more portable

-   Edited buildignore to include some files that don't need to be made available in package

-   Added a couple options to default devtools::check/R CMD check settings so life is a bit easier in the pre-CRAN submission era

-   Moved the `explanations` and `explain_short` objects into an internally stored list called `R/sysdata.rda` to fix some NOTES from devtools::check(). I've added a script to recreate the data file in `data-raw/explanations.R`.

-   Removed calls from `summary_table_check` to `summary_table_update`. Basically, the only way that the user could not have the `summary_table.rda` file in their *extdata* folder is if they intentionally deleted it (it's installed as part of the package, so it should always be there). Additionally, if they have chosen to delete it, I assume they had a good reason to do so. Instead, I've exported the table's check function so anyone can use it to see how out of date they are. They can then call the update function manually instead. **Disclaimer: there are probably bugs in this reorganization**
