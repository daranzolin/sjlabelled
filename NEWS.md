# sjlabelled 1.0.6

## Changes to functions

* `get_dv_labels()` and `get_term_labels()` now support `clm`-objects from package *ordinal*,  `polr`-objects from package *MASS* and `Zelig-relogit`-objects from package *Zelig*.
* `get_dv_labels()` and `get_term_labels()` get a `...`-argument to pass down further arguments to `snakecase::to_any_case()`.
* `convert_case()` is now exported, for usage in other packages as well.
* Remove `protect`-argument from internal case conversion (affects `get_term_labels()` and `get_dv_labels()`), in preparation for forthcoming *snakecase*-package update.

# sjlabelled 1.0.5

## General

* Remove unnecessary imports.
* Revised `lbl_df()` due to changes in the internals of `tibble::trunc_mat()`.

## New functions

* `as_factor()` to convert labelled vectors into factors, preserving labels.

## Changes to functions

* `get_dv_labels()` now supports `brmsfit`-objects from package `brms`.

# sjlabelled 1.0.4

## Changes to functions

* `get_term_labels()` now includes variable names for factors with numeric factor levels only (and not only return the numeric level as term label).

## Bug fixes

* Fixed bug for `as_label()`, when `x` was a character vector and argument `drop.levels` was `TRUE`.
* Fixed issue for *lme* and *gls* objects in `get_term_labels()` and `get_dv_labels()`.

# sjlabelled 1.0.3

## General

*  Changed package imports, so `sjlabelled` no longer requires R version 3.3.3 or higher.

# sjlabelled 1.0.2

## General

* Minor fix to avoid warning when using `as_numeric()`.

## Changes to functions

* `get_label()`, `get_term_labels()` and `get_dv_labels()` get a `case`-argument, to convert labels into any case, using the [snakecase](https://cran.r-project.org/package=snakecase)-package.

# sjlabelled 1.0.1

## General

* Removed function 'var_rename()', which is in pkg 'sjmisc'.

## New functions

* `get_term_labels()` and `get_dv_labels()` to retrieve term labels from regression models.

## Changes to functions

* `as_numeric()` gets a `use.labels`-argument to use value labels as new values if these are numeric.

# sjlabelled 1.0.0

## General

* Initial release. All labelled data utility functions from package *sjmisc* have been moved to this package, which is now dedicated to tools for working with labelled data.