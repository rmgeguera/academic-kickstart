# UMass Joint Labs Fork of the [Academic Kickstart](https://sourcethemes.com/academic/) theme for Hugo

**Academic** is a Hugo theme created by George Cushen.
- [**Get Started**](#install)
- [View the documentation](https://sourcethemes.com/academic/docs/)
- [Ask a question](http://discuss.gohugo.io/)
- [Request a feature or report a bug](https://github.com/gcushen/hugo-academic/issues)
- Updating? View the [Update Guide](https://sourcethemes.com/academic/docs/update/) and [Release Notes](https://sourcethemes.com/academic/updates/)
- Support development of Academic:
  - [Donate a coffee](https://paypal.me/cushen)
  - [Become a backer on Patreon](https://www.patreon.com/cushen)
  - [Decorate your laptop or journal with an Academic sticker](https://www.redbubble.com/people/neutreno/works/34387919-academic)
  - [Wear the T-shirt](https://academic.threadless.com/)

[![Screenshot](https://raw.githubusercontent.com/gcushen/hugo-academic/master/academic.png)](https://github.com/gcushen/hugo-academic/)

## Ecosystem

* **[Academic Admin](https://github.com/sourcethemes/academic-admin):** An admin tool to import publications from BibTeX or import assets for an offline site
* **[Academic Scripts](https://github.com/sourcethemes/academic-scripts):** Scripts to help migrate content to new versions of Academic


## Install

You'll need [python3](https://www.python.org/downloads/) and [hugo](https://gohugo.io/) to get everything up and running. If you're going to fiddle around with BibTex

You can choose from one of the following four methods to install:

* [**one-click install using your web browser (recommended)**](https://sourcethemes.com/academic/docs/install/#install-with-web-browser)
* [install on your computer using **Git** with the Command Prompt/Terminal app](https://sourcethemes.com/academic/docs/install/#install-with-git)
* [install on your computer by downloading the **ZIP files**](https://sourcethemes.com/academic/docs/install/#install-with-zip)
* [install on your computer with **RStudio**](https://sourcethemes.com/academic/docs/install/#install-with-rstudio)

Then [personalize your new site](https://sourcethemes.com/academic/docs/get-started/).

## Editing the site

1. INITIAL SETUP. open `_default/config`, `/params`:

in `_default/config`:
- change title of site to your name

in `_default/params`:
- change description of site
- add an image to show up if your site is searched for if you want
- edit contact widget info if you want

2. DECIDE WHAT SECTIONS YOU WANT. open `_default/menus`:

If you like having an all-in-one About section, go to `content/author/index` and edit that information.
Otherwise, open `content/home/about` and change active to false to get rid of it.

3. DEAL WITH PUBLICATIONS. 

- export a bibtex file
- download the academic export script using pip: 
`pip3 install -U academic
academic import --bibtex path/to/bibtex`
- deal with any issues where the date is missing/'in prep'
- decide whether you want to feature any publications or not -- you'll have to change featured to true 
- also decide whether you want to tag any of this 

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/sourcethemes/academic-kickstart/blob/master/LICENSE.md) license.
