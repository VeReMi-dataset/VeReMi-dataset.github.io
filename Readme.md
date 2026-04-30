# VeReMi-dataset.github.io

See [VeReMi-dataset.github.io](https://veremi-dataset.github.io).

## Making Changes to the Website

This site is using Jekyll to generate webpages from Markdown and then gh-pages to deploy them. 
However, we are not using automatic deployment tools (old gh-pages or Actions) from GitHub. 

### Requirements

 * jekyll, theme and dependencies for building the page (see Gemfile)
 * npm module `gh-pages` for deploying (see package.json)


 ### Submitting and Deploying Changes

  After making the changes to the source of the website, run the following command to re-build the pages:

  ```bash
  bundle exec jekyll build
  ```

  This will place the page in the `_site/` folder. Next, we use `gh-pages` to move the contents of `_site/` to the `gh-pages` branch of this repo:

  ```bash
  npm run deploy
  ```