---
name: R package code review
about: This is meant to serve as a template for conducting a code review for an R
  package going into the toolbox.
title: 'Code review: R package - '
labels: ''
assignees: ''

---
## Code Review Template for an R Package
This issue template should be filled out when a new R package is onboarded to the Fisheries Integrated Toolbox. For each item, please check the appropriate box and outline any changes that need to be made to the package to improve an issue. If issues are uncovered, document them below the item on the list.

#### Installation and build
1. Install package. Use `remotes::install_github(dependencies = TRUE)` to ensure you have all of the dependencies needed for the package. 
- [ ] works
- [ ] issues uncovered

2. Run `devtools::check()`. This mimics the CRAN check functionality, and if you want to upload your package to CRAN, this must succeed with no errors and no warnings. This builds the package and runs all tests.
- [ ] works
- [ ] issues uncovered

#### Documentation
3. `devtools::run_examples()` checks that all exported function examples run successfully locally.
- [ ] works
- [ ] issues uncovered

4. Comprehensive installation instructions for the recommended package version are included in the README.
- [ ] works 
- [ ] issues uncovered

5. All exported functions have properly formatted documentation.
- [ ] works
- [ ] issues uncovered

6. There is a user guide or a vignette that walks the user through an example, and the vignette code all runs successfully.
- [ ] works
- [ ] issues uncovered


#### Structure
7. Package conforms to R package structure as defined below (from [Writing R Extensions](https://cran.r-project.org/doc/manuals/r-release/R-exts.html#Package-structure)):
> The sources of an R package consist of a subdirectory containing the files DESCRIPTION and NAMESPACE, and the subdirectories R, data, demo, exec, inst, man, po, src, tests, 
> tools and vignettes (some of which can be missing, but which should not be empty). The package subdirectory may also contain files INDEX, configure, cleanup, LICENSE, LICENCE > and NEWS. Other files such as INSTALL (for non-standard installation instructions), README/README.md, or ChangeLog will be ignored by R, but may be useful to end users.
- [ ] works
- [ ] issues uncovered

8. Check dependencies
```
install_github("falo0/dstr")
library(dstr)
dstr()
```
- [ ] works
- [ ] issues uncovered

9. Check that exports make sense. For example, are data sets and objects that are only used internally exported? Or only functions that would likely be used?
```
getNamespaceExports()
```
- [ ] works
- [ ] issues uncovered

#### NOAA specific
10. The LICENSE corresponds to the approved NOAA wording:
> “Software code created by U.S. Government employees is not subject to copyright in the United States (17 U.S.C. §105). The United States/Department of Commerce reserve all
> rights to seek and obtain copyright protection in countries other than the United States for Software authored in its entirety by the Department of Commerce. To this end, the
> Department of Commerce hereby grants to Recipient a royalty-free, nonexclusive license to use, copy, and create derivative works of the Software outside of the United
> States.”
- [ ] works
- [ ] issues uncovered

11. All contributors have NOAA accounts and push access is disabled for non-NOAA collaborators.
- [ ] works
- [ ] issues uncovered

12. Two-factor authentication is set up for all account contributors.
- [ ] works
- [ ] issues uncovered


#### General comments
