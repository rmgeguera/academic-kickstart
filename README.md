# UMass Joint Labs Fork of the [Academic Kickstart](https://sourcethemes.com/academic/) theme

## What's Academic?

**Academic** is a theme for Hugo created by George Cushen.
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

### Ecosystem

* **[Academic Admin](https://github.com/sourcethemes/academic-admin):** An admin tool to import publications from BibTeX or import assets for an offline site
* **[Academic Scripts](https://github.com/sourcethemes/academic-scripts):** Scripts to help migrate content to new versions of Academic

## Get your site running

See the demo site [here](http://people.umass.edu/rgeguera). [For more help, see the Academic docs.](https://sourcethemes.com/academic/docs/install/)

### Prerequisites

You'll need [hugo](https://gohugo.io/getting-started/installing) to get everything up and running. If you use [homebrew](https://brew.sh/) (Mac), [chocolatey](https://chocolatey.org/) (Windows), or [scoop](https://scoop.sh/) (Windows), it's as easy as `brew|chocolatey|scoop install hugo`. Otherwise, grab the appropriate binary from [here](https://github.com/gohugoio/hugo/releases), extract it into directory structure `Hugo/bin` and run it. To check that you have both of those things, open a terminal/windows powershell and type in `hugo`. 

### Initial setup

If you use git, the easiest way to do this is to clone it: `git clone https://github.com/rmgeguera/academic-kickstart.git my_site`, `cd my_site`, `git submodule update --init --recursive`.

OR: 

1. Download this fork as a .zip or .tar and extract it into the folder of your choice, e.g. `Desktop/academic-kickstarter-master` (feel free to rename the folder -- I've renamed my example to `xling-demo`). 
2. Download the [Academic theme](http://people.umass.edu/rgeguera/files/academic.zip) and extract it into `Desktop/xling-demo/`. Rename it to `academic` and move it into `xling-demo/themes`.
3. In a terminal, navigate to your site's root directory (for me, `cd Desktop/xling-demo/`) and type in `hugo server`. The structure of your root directory should look like this:

```
your-site
	config -- this is all the configuration/settings info
	content -- the content for each section is here!
	data -- fonts, themes
	resources
	scripts
	static -- stash things you want to share, like background images or a CV
	themes
		academic 
	.editorconfig
	.gitignore if you used git
	.gitmodules if you used git
	License.md
	README.md
	netlify
	update_academic.sh
	view.sh
```

If all went well, you'll see a message that your web server is available at localhost:1313. Enter that into a web browser, and you should see the exact same demo. 

Then [personalize your new site](https://sourcethemes.com/academic/docs/get-started/)!

## Editing the site

Each visible section of your website corresponds to a markdown file. The setup of most files which comprise your site will be TOML at the top, which configures whatever content you have after the +++ in Markdown. The most critical thing to edit is whether each page is active or not: `active = true` means it'll display on your site, and `false` means it won't show up.

The first thing to do is adjust the settings or configuration:

1. Open `xling-demo/config/_default/`.

in `_default/config`:
- change title of site to your name
- change baseURL to either your github ([username].github.io) or your UMass site (remember the slash at the end!!)

in `_default/params`:
- change description of site
- add an image to show up if your site is searched for if you want (change from ducks.jpg)
- edit contact widget info if you want

2. Decide what sections you want. Open `_default/menus`:

If you like having an all-in-one About section, go to `content/author/index` and edit that information.
Otherwise, open `content/home/about` and change active to false to get rid of it.

3. Deal with publications/papers. You'll need [python3](https://www.python.org/downloads/) for this. 

- export a bibtex file of your work
- download the academic export script using pip: 
`pip3 install -U academic
academic import --bibtex path/to/bibtex`
- deal with any issues where the date is missing/'in prep'
- decide whether you want to feature any publications or not -- you'll have to change featured to true 
- also decide whether you want to tag any of this 

You can also just create publications on your own -- create a folder manually or enter `hugo new --kind publication publication/[author]-[year]`. You should fill out:
- title
- authors
- summary
- publication type
- abstract if you have it
- tags if you want (must look-like-one-thing to generate a page with all the tagged posts)

## License

Copyright 2017-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/sourcethemes/academic-kickstart/blob/master/LICENSE.md) license.
