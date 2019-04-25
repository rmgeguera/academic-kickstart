# [UMass Joint Labs Fork](http://people.umass.edu/rgeguera) of the [Academic Kickstart](https://sourcethemes.com/academic/) theme

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

[For more help, see the Academic docs.](https://sourcethemes.com/academic/docs/install/)

### Prerequisites

You'll need [python3](https://www.python.org/downloads/) and [hugo](https://gohugo.io/) to get everything up and running. To check that you have both of those things, open a terminal/windows powershell and type in `python3` and `hugo`. 

First, clone this repository, or just download the zip and extract it into the folder of your choice so that you get something like `Documents/academic-kickstarter-master` (feel free to rename the folder -- I've renamed my example to `xling-demo`. Then download the [Academic theme](https://github.com/gcushen/hugo-academic/archive/master.zip) and extract it into `Documents/xling-demo/themes/`. Delete the empty folder and rename the one with things actually in it to `academic`.

In a terminal, navigate to your site's root directory (for me, `cd Documents/xling-demo/`) and type in `hugo server`. If all went well, you'll see a message that your web server is available at localhost:1313. Enter that into a web browser, and you should see the exact same demo. 

Then [personalize your new site](https://sourcethemes.com/academic/docs/get-started/)!

## Editing the site

### Initial Setup

1. Open `xling-demo/config/_default/config`, `/params`:

in `_default/config`:
- change title of site to your name
- change baseURL to either your github ([username].github.io) or your UMass site

in `_default/params`:
- change description of site
- add an image to show up if your site is searched for if you want (change from ducks.jpg)
- edit contact widget info if you want

2. Decide what sections you want. Open `_default/menus`:

If you like having an all-in-one About section, go to `content/author/index` and edit that information.
Otherwise, open `content/home/about` and change active to false to get rid of it.

3. Deal with publications/papers. 

- export a bibtex file of your work
- download the academic export script using pip: 
`pip3 install -U academic
academic import --bibtex path/to/bibtex`
- deal with any issues where the date is missing/'in prep'
- decide whether you want to feature any publications or not -- you'll have to change featured to true 
- also decide whether you want to tag any of this 
- you can also just create publications on your own -- create a folder 

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/sourcethemes/academic-kickstart/blob/master/LICENSE.md) license.
