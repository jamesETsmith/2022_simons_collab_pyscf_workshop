# Contributing

Contributions in the form of bug fixes or new tutorials are always welcome! Please open an issue or pull request after consulting the guidelines below.

## Guidelines

Please remove the meta data from all jupyter notebooks in `demos` before pushing your changes. This meta data can cause the size of the repo to grow rapidly and make `git diff` harder or impossible to interpret. We suggest using [`nb-clean`](https://github.com/srstevenson/nb-clean) (`pip install nb-clean`) along with the pre-commit hook below (don't forget to make it executable):

```bash
#!/usr/bin/env bash

# date: 2022-06-16
# author: James E. T. Smith <james.smith9113@gmail.com>
# filename: .git/hooks/pre-commit

# Don't forget to make this file executable!

echo "About to clean jupyter notebooks with nb-clean"

# Clean files
nb-clean clean demos/*.ipynb

# Add back the modified files
git add demos/*.ipynb

```