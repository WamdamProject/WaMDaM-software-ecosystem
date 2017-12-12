# WaMDaM Docs Generator

## Installation

This project is built upon a themed version of `mkdocs` named [material-mkdocs][https://squidfunk.github.io/mkdocs-material/].

First you need to install (as root) pip on your machine

```
apt install python-pip
```

then you can install `mkdocs-material`

```
pip install mkdocs-material
```

## Commands

* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    site/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Project customizations

For the purposes of this project the following changes were made:

* The default folder for the markdown and static files is set to `site`
* The folder where the actual docs will be generated is set to `docs`, in order to match the configuration project on github pages


## Adding new pages to docs

It's really simple, just create a new markdown file on the `site` folder, then add the content you wish to be displayed on this page.

## Page titles and order

You can also customize the title and order in which the pages are displayed on the side menu. By default each entry would take the name of the first title section on the file. You can change these names and order by adding a section named `pages` on the `mkdocs.yml` file. E.g:

```
pages:
  - Home: index.md
  - Installation: installation.md
  - Features: features.md
  - About: about.md
```