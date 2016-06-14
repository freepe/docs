# Barricade Docs

[![CircleCI](https://circleci.com/gh/barricadeio/docs.svg?style=svg)](https://circleci.com/gh/barricadeio/docs)

[docs.barricade.io](https://docs.barricade.io), built as a static site with [Hugo](http://gohugo.io/).

![https://cloud.githubusercontent.com/assets/686194/12189426/550f84e4-b572-11e5-821a-3b4d517b1642.png](https://cloud.githubusercontent.com/assets/686194/12189426/550f84e4-b572-11e5-821a-3b4d517b1642.png)

--

New content is added by adding Markdown files to the `/content` subdirectories.
New images and other media should be located in `themes/barricade/static/src`.

--

# Local Development

The user manual for Barricade is built with Hugo, the API docs with Middleman.

* Run `hugo server --watch` to generate the site
* Run `bundle exec middleman build --clean` in api directory
* In a different window, run `gulp watch` to compile assets
* The site will be available at [localhost:1313](http://localhost:1313/)

# Deploying

Master is automatically deployed to Github Pages via CircleCI.
