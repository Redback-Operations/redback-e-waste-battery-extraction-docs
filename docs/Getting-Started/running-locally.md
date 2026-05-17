---
title: Running Mkdocs Locally
---

# Local Environment

If you wish to run MkDocs locally to see how your document may appear in GitHub without using other tools such as Markdown extensions the below steps outline the Python setup process.

## Linux

!!! info "You will need to clone the repoistory first."

1. Creating virtual Python environment 
```Bash
python3 -m venv env
```
2. Activate the environment
```Bash
source env/bin/activation
```
3. Install Mkdocs and supporting libraries 
```Bash
pip3 install mkdocs mkdocs-material mkdocs-awesome-pages-plugin

```

The following command runs MkDocs local instance with live reloading of any page changes.
```Bash
mkdocs serve --livereload
```
