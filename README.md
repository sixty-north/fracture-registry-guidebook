# Fracture Registry Guidebook

This document is a guidebook for developers of the Norwegian Fracture Registry.

## Install the dependencies

This documentation is written using [Sphinx](http://www.sphinx-doc.org/), a
powerful documentation system written in Python. As such, you'll first need to
make sure you have [Python 2.7+ or 3+](http://python.org) installed on your
system.

Once you've got Python installed, you need to install Sphinx and some related
dependencies. These are listed in `requirements.txt`, and the simplest way to
install them is with `pip`:

```
pip install -r requirements.txt
```

## Build the HTML documentation

Once these dependencies are in place, you need to build the documentation from
the reStructured Text and Markdown source files. On Unix/Linux/OSX you can use
the provided `Makefile` via `make`:

```
make html
```

On Windows you'll need to use the provided `make.bat`:

```
make.bat html
```

If everything goes smoothly, the output will be the `build` directory. You can
open up `build/html/index.html` in your browser to view it.

## Hosting on github

We currently host the built version of these docs on sixty-north.github.io. As
we make changes, we should redeploy there. To do that, run `make html`, copy the
results from `build/html` to the correct (hopefully obvious) location in the
deployment repo, and push them up. It should be that simple.
