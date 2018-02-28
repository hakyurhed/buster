# Buster

[![Docker Pulls](https://img.shields.io/docker/pulls/unsettling/buster.svg)](https://microbadger.com/images/unsettling/buster)
[![Docker Stars](https://img.shields.io/docker/stars/unsettling/buster.svg)](https://microbadger.com/images/unsettling/buster)
[![Docker Image Size](https://images.microbadger.com/badges/image/unsettling/buster.svg)](https://microbadger.com/images/unsettling/buster)
[![Docker Version](https://images.microbadger.com/badges/version/unsettling/buster.svg)](https://microbadger.com/images/unsettling/buster)
[Docker Hub](https://hub.docker.com/r/unsettling/buster/)  

Super simple, totally awesome, brute force **static site generator for**
[Ghost](http://ghost.org/).

Start with a clean, no commits Github repository.

*Generate Static Pages. Preview. Deploy to Github Pages.*

Warning! This project is a hack. It's not official. But it works for me.

## About this fork

This is a work in progress containing many of the pull requests made to the
original buster repo (which unfortunately has been abandoned by its author).

It includes most of the changes by

* skosch
* petemichel77
* Misiur
* Jeongseok Son
* raccoony
* leftofnull
* alokard

It should also work with static pages (e.g. `about`, `tag/...`, etc.).

There may well be issues still, especially around Windows compatibility; I'm
happy to merge your PRs.

## Installation

With `pip` installed, simply run

    pip install git+https://github.com/boggin/buster

You could also just clone the source and use the `buster.py` file directly.

## The interface

    setup [--gh-repo=<repo-url>]

Creates a GIT repository inside `static/` directory.

    generate [--domain=<local-address>]

Generates static pages from locally running Ghost instance.

    preview

Preview what's generated on `localhost:9000`.

    deploy

Commits and deploys changes static files to Github repository.

    add-domain <domain-name>

Adds CNAME file with custom domain name as required by Github Pages.

Buster assumes you have `static/` folder in your current directory (or
creates one during `setup` command). You can specify custom directory
path using `[--dir=<path>]` option to any of the above commands.

Don't forget to change your blog URL in config.js in Ghost.

## Requirements

* wget: Use `brew install wget` to install wget on your Mac.
   Available by default on most linux distributions.

* git: Use `brew install git` to install git on your Mac.
   `sudo apt-get install git` on ubuntu/debian

The following python packages would be installed automatically when
installed via `pip`:

* `docopt <https://github.com/docopt/docopt>`: Creates beautiful
   command line interfaces *easily*.
* `GitPython <https://github.com/gitpython-developers/GitPython>`:
   Python interface for GIT.

## Ghost. What?

[Ghost](http://ghost.org/features/) is a beautifully designed,
completely customisable and completely open
source **blogging platform**. If you haven't tried it out yet, check it out. 
You'll love it.

The Ghost Foundation is not-for-profit organization funding open source
software and trying to completely change the world of online publishing.

## Buster?

Inspired by THE GhostBusters.

![Ghost Buster Movie Poster](https://upload.wikimedia.org/wikipedia/commons/thumb/1/12/Lego_Ghostbusters_%282914485906%29.jpg/320px-Lego_Ghostbusters_%282914485906%29.jpg?uselang=en-gb)

## Contributing

Checkout the existing [issues](https://github.com/boggin/buster/issues) or create a new one. Pull requests welcome (actually, this time)!
