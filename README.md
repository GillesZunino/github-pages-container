# GitHub Pages Development Container

## Installation and Startup
1. Navigate to `https://pages.github.com/versions/`. This page lists all GitHub Pages dependencies,
2. In `Dockerfile`, set `RUBY_VERSION` to the version expected by GitHub Pages,
3. In `Gemfile`, ensure the version of various gems matches the ones expected by GitHub Pages. Specifically, `"github-pages`, `minima` must match,
4. In Visual Studio Code, open this directory in a dev container,
5. Open a shell in the container and run `bundle install`,
6. Start the Jekyll server with `bundle exec jekyll serve --livereload --incremental`.

## Adding Content
Add markdown pages, content and static assets directly at the root of the repo or in subdirectories like `pages`.

## Tips and Tricks

1. Add plugins to `group :jekyll_plugins do` in `Gemfile`,
2. Edit `_config.yml` to change Jekyll behavior,
3. A theme can be copied and modified as follows:
    * `bundle info jekyll-theme-cayman` to retrieve the `path` of the theme,
    * `cp <path>/. . -p -r`. This *might* replace some files like `LICENSE` or `README.md`,
    * Make changes to files under `_layouts`, `_includes`, `assets`, ...