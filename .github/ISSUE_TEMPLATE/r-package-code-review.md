---
name: R package code review
about: This is meant to serve as a template for conducting a code review for an R
  package going into the toolbox.
title: 'Code review: R package - '
labels: ''
assignees: ''

---

1. Install package.
- [ ] works
- [ ] issues uncovered

2. Run `devtools::check()`

3. Check dependencies
```
install_github("falo0/dstr")
library(dstr)
dstr()
```

4. Check exports
```
getNamespaceExports(mmrefpoints)
````

4. `devtools::run_examples()`
