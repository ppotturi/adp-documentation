# adp-documentation
Public Azure Developer Platform Documentation for Defra


# Running locally on windows

## Virtual Env

https://docs.python.org/3/tutorial/venv.html

Run
```
python -m venv venv
```
Run (windows)
```
venv\Scripts\activate
```

install/ upgrade pip
```
python -m pip install --upgrade pip
```

```
pip install mkdocs-material
```


To deactivate virtual environment `deactivate`


# MK Docs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.