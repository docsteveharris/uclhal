## 2021-12-20
Running log of steps used 
Each time you do some work enter the date on a new line
Then one line per statement thereafter
https://python-poetry.org/docs/basic-usage/

set up poetry
```sh
poetry new uclhal
poetry add nikola
poetry shell
```

git
```sh
git init
git branch -m main
```

https://getnikola.com/getting-started.html
conflicts if you run the set up command from the root of the poetry project
maybe something to do with their being a toml file there already?
instead I did the install from a clean (naked) subdirectory
site at ./uclhal/uclhal

?prob will need to publish the site from that subdirectoy if I wish to use github



## 2021-12-21
set up pylsp in sublime

updated pyproject.toml
```toml
[tool.poetry.dev-dependencies]
pytest = "^5.2"
python-lsp-server = "^1.3.1"
python-lsp-black = "^1.0.0"
mypy-ls = "^0.5.1"
pyls-isort = "^0.2.2"
```
then
```sh
poetry update
```

then
copied settings from dashRep into uclhal.sublime-project
used `which pylsp` to find the path to pylsp
```json
	"settings": {
        "LSP": {
            "pylsp": {
                "enabled": true,
                "command": [
                    "/Users/steve/Library/Caches/pypoetry/virtualenvs/uclhal-XMZ_bNmG-py3.9/bin/pylsp",
                ],
                "settings": {
                    "pylsp.plugins.flake8.executable": "/Users/steve/Library/Caches/pypoetry/virtualenvs/uclhal-XMZ_bNmG-py3.9/bin/flake8",
                },
            },
        },
    },
```


deploy to github
uses the following tool
https://github.com/c-w/ghp-import

> Inside your repository just run ghp-import $DOCS_DIR where $DOCS_DIR is the path to the built documentation. This will write a commit to your gh-pages branch with the current documents in it.

