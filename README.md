# IPTC Doctest2 - using MkDocs

This repository is made for testing the maintenance of documenting an IPTC standard by i/ a Github respository with a gh-pages branch and the associated web server and ii/ [MkDocs](http://www.mkdocs.org/) as tool for creating the HTML content.

The files in the gh-branch of this repository are displayed on the web site [https://iptc.github.io/doctest3](https://iptc.github.io/doctest3)

Setup of the repository:

* master branch: holds files for controlling MkDocs and the files for creating the content by MkDocs in the docs folder = the raw files of the content
* gh-pages branch: holds the HTML rendition files for use by the Github webserver. They have been created by a local instance of MkDocs which is set up by one of the editors of the content.

Workflow for the local editing of content:

* Create a local repository of this repository's master branch.
* Create a local repository of this repository's gh-pages branch. (Recommended: create a gh-pages sub-folder in the master branch's main folder the root of the gh-pages branch and include "gh-pages/" in the .gitignore file of the master branch, if it is not there already.)
* Edit the files holding the content (in the master branch, docs folder)
* Create an updated version of the HTML renditions in the folder of the gh-pages branch (by: `mkdocs build --clean`)
* Push these updated files to this repository's gh-pages branch.
