# Curitiba BitDevs

Simple Jekyll site for hosting all of the links from meetups past and future.

## Development

You'll need [Ruby & Jekyll](https://jekyllrb.com/docs/installation/) to run the
site locally.

For Linux:
* Run `sudo apt install ruby ruby-dev build-essential`
* Run `export PATH="$(ruby -r rubygems -e 'print Gem.user_dir')/bin:$PATH" bundle install`
* Run `gem install --user-install bundler -v 2.6.6`
* Run `bundle config get path`

Once they're setup:

* Clone the repository and go into the directory
* Run `bundle install`
* Run `bundle exec jekyll serve`
* Go to http://localhost:4000

## Making a Post

To make a new post, create a new file in `_posts/` based on the [template](_posts/_template.md) with a title of
`YYYY-MM-DD-title-goes-here`. At the top of the file you'll want to provide the
following information:

```md
---
layout: post # Always post
type: socratic # or whitepaper for a whitepaper series
title: "Name of the Post"
meetup: https://www.meetup.com/curitiba-bitdevs/events/[event id here]/
---
```

Commit message example: feat(posts): add nov 2025
After that, it's just simple markdown. The site will auto-generate the rest.

## Changing Site Data

All site configurations are either contained in `_config.yml` or
`_data/settings.yml`. Some data is duplicated between the two due to the way
Jekyll injects variables, so be sure to update both.

## Attributions

Thanks to [LeNPaul](https://github.com/LeNPaul/jekyll-starter-kit) for the
Jekyll starter kit this was forked from.
