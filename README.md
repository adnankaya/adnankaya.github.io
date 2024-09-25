## Installation and Run

```bash
# install dependencies
pip install -r requirements.txt

# run
mkdocs serve
# build the site
mkdocs build

# deployment to github
mkdocs gh-deploy --force


```

### ERRORS
1. cannot find module 'ext.slugs' (No module named 'ext')
Solution: add your current directory with `export PYTHONPATH=.` on a UNIX-like terminal.