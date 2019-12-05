# level0

## Description
The `level0` package is a collaborative effort in the R programming language to create error checks and visualizations for the eScholar extracts used for educational data reporting in New York State.  It depends on the `dBtools` package [located here](https://github.com/debarros/dBtools) and the `openxlsx` package [available on CRAN](https://cran.r-project.org/package=openxlsx).
### Initial Scope
The initial goal for the package will be to replicate all of the Level 0 error checks.
### Long Term Scope
The long term goal for the package will be to create an ever-evolving tool to assist data coordinators in New York.  New functions, error checks, and visualizations will be added by useRs throughout the state.
## Structure and Naming Conventions
### Style
The package will (try to) follow the [guidelines for R packages laid out by Hadley Wickam](https://r-pkgs.org/).
### Function Types and Names
Initially, there will be four types of functions.  Each function will handle either a single extract or multiple extracts, and handle them from a single point in time or from multiple points in time.  In addition, the single-extract, single-time point functions will either handle columns individually or will compare columns.  Single-extract, single-time-point functions will be named by the extract they are intended to analyze, followed by an underscore and then `SingleCol` or `MultiCol`.
- Single-export, single-time-point 
  - Single column functions (e.g. `StudentLite_SingleCol()`)
    - Check for missing values
    - Check for values in unused columns
    - Check for duplicates
    - Check for unacceptable values
  - Multiple column (e.g. `StudentLite_MultiCol()`)
    - Check Both-or-neither situations
    - Check duplicates-across-columns (e.g. race)
    - Compare dates
 - Multiple-export, single-time-point functions
   - Subtypes and functionality to be determined
 - Single-export, multiple-time-point functions
   - Subtypes and functionality to be determined
 - Multiple-export, multiple-time-point functions
   - Subtypes and functionality to be determined
 
