questionr 0.7.5
---------------




questionr 0.7.4
---------------

* Add `useNA` and deprecate `na.rm` and `na.show` arguments to `wtd.table` (thanks @nalimilan)
* Add `fct_relevel` method to `iorder` (thanks @nalimilan)
* New function `ggsurvey()` for easy plots with `survey` objects and 
  `ggplot2` (#123, @larmarange)


questionr 0.7.3
---------------

* Remove `dplyr::recode` method from `irec` as it is in questioning lifecycle
* Fix `forcats` and `dplyr` detection in `irec` (thanks @matthias-studer)
* Fix R.cache blocking message in `irec`, `icut` or `iorder` (thanks @matthias-studer)
* Fix name conflicts when `irec`, `icut` or `iorder` are called with a data frame with the same name as a function (thanks @nalimilan)
* Sort level names in `irec` and `iorder` instead of relying on `unique` (thanks @nalimilan)


questionr 0.7.2
---------------

* `look_for()` and `lookfor()` are now simply imported and reexported 
  from `labelled` (#111, @larmarange)


questionr 0.7.1
---------------

* `fertility` and `fecondite` datasets imported with haven 2.3.0 (thanks @larmarange)
* Fix irec fct_recode code when there is a space in variable name
* Remove obsolete `wtd.var` function. Use `Hmisc::wtd.var` instead.
* Improve styling of code generated by iorder, irec and icut
* Fix error when both "NA" and NA in a vector passed to `freq`
* Use `dplyr::recode_factor` instead of using `factor()` (thanks @larmarange)


questionr 0.7.0
---------------

* Compatibility with `labelled` 2.0.0


questionr 0.6.3
---------------

* Make `rprop`, `cprop` and `prop` compatible with `janitor::tabyl` for pipeline integration
* Replace `R2HTML::HTML` with `knitr::kable` in `clipcopy`
* Fix incorrect NAs percentage in `describe` (thanks @gdutz)
* Add new tabs() function (thanks @rdrr1990)


questionr 0.6.2
---------------

* Add `exclude` argument to `wtd.table` (thanks @pgtpg)
* Make `clipcopy` work with tibbles
* Bugfix : missing rownames in `iorder` verification table
* Generate a `pkgdown` package documentation at https://juba.github.io/questionr/
* Fix incompatibility between `cum`, `sort` and NAs in `freq` (thanks @scoavoux)
* Bugfix : error when recoding a numeric variable with `forcats` in `irec`


questionr 0.6.1
---------------

* New "Recoding addins" vignette
* Add support for `forcats::fct_recode` in `irec`
* Add support for `dplyr::recode` in `irec`
* "Variable cutting" addin entry renamed to "Numeric range dividing"
* Bugfix : conflict between `useNA` and `exclude` in `freq` (thanks @scoavoux)
* Bugfix : Fix missing rownames in icut table results


questionr 0.6.0
---------------

* New `na.rm` argument to `cross.multi.table`. Use `na.rm = FALSE` to display NA level in `crossvar`
* New `rp2012` dataset
* New `fertility` dataset (@larmarange)
* New `ltabs` function, for labelled variables cross-tabulation (@larmarange)
* `describe`, `lookfor` and `freq` are harmonized and now work with `labelled` variables (@larmarange)
* Integration with the `labelled` package (@larmarange)
* `freq` added to `describe` (@larmarange)
* More detailed `lookfor` results (@larmarange)


questionr 0.5.0
---------------

* `irec`, `icut` and `iorder` have been converted to RStudio addins. They now work both with vectors and data frames.
* Bugfix : handle regexp special chars in variable or split character in multi.split (thanks @markriseley)
* `irec` allows to select the type of output : character, factor or numeric (thanks @larmarange)
* `irec` now works with numeric variables
* Bugfix : name conflicts with global environment objects (thanks @scoavoux)
* `irec` now trims leading and trailing whitespaces in inputted values
* Minimal recoding style by default in `irec`
* Fix false positives in multi.split (thanks @markriseley)
* New fecondite labelled dataset (thanks @larmarange)
* New happy dataset (thanks @briatte)
* cross.multi.table() now accept a `n` argument to display the total number of
  observations by row or column (when `freq=TRUE`).


questionr 0.4.3
---------------

* cross.multi.table() now accept a `tfreq` argument to display row percentages 
  based on the (potentially weighted) contingency table of respondants.
* Fix : i* interactive functions now work with data.table and dplyr's tbl_df

questionr 0.4.2
---------------

* cross.multi.table() now accept a `freq` argument to display column percentages 
  based on the (potentially weighted) contingency table of crossvar on respondants. 
* multi.table() now accept a `freq` argument to compute percentages based on 
  (potentially weighted) number of repondants. Note that `freq` is set to TRUE
  by default
* Fix : wrong HTML() call in clipcopy()
* Refactoring : icut, irec and iorder are now shinyApps functions
* Translation : icut, irec and iorder interfaces are now translated in french

questionr 0.4.1
---------------

* Bugfix : compatibility with shiny 0.10

questionr 0.4
---------------

* New functions from Joseph Larmarange : duplicated2, na.rm, rm.unused.levels
* Default lookfor `keywords` argument changed to "" (displays all variables)
* New argument `n` to cprop and rprop to display the number of observations
  per row/column
* "Ensemble" and "Total" strings in cprop and rprop are now localized
* Bugfixes on irec : encoding on windows and empty strings in factor levels
* `freq` now displays, by default, a column of percentage based on
  non-missing values 

questionr 0.3.1
---------------

* Bugfix : weights handling in cross.multi.table
* Bugfix : NA values in icut

questionr 0.3
-------------

* New functions from Joseph Larmarange : addNAstr and odds.ratios
* copy renamed to clipcopy to avoid name collisions with data.table
* New function : icut, interactive shiny interface for `cut`
* New function : iorder, interactive shiny interface for ordering the levels of a factor
* New function : irec, interactive shiny interface for recoding a variable

questionr 0.2
-------------

* New functions : describe, freq.na, qload, qscan, recode.na
* Finish transition from rgrs

questionr 0.1
-------------

* First version