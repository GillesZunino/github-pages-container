# -----------------------------------------------------------------------------------
# Copyright 2024, Gilles Zunino
# -----------------------------------------------------------------------------------

# ========================================================================
# GitHub Dependencies => https://pages.github.com/versions/
# ========================================================================
source "https://rubygems.org"

# Bundler
gem "nokogiri"
gem "rack", "~> 2.2.4"
gem "rspec"

# GitHub Pages
gem "github-pages", "~> 232", group: :jekyll_plugins

# Themes for new Jekyll sites
gem "minima"

gem "jekyll-theme-architect"
gem "jekyll-theme-cayman"
gem "jekyll-theme-dinky"
gem "jekyll-theme-hacker"
gem "jekyll-theme-leap-day"
gem "jekyll-theme-merlot"
gem "jekyll-theme-midnight"
gem "jekyll-theme-minimal"
gem "jekyll-theme-modernist"
gem "jekyll-theme-primer"
gem "jekyll-theme-slate"
gem "jekyll-theme-tactile"
gem "jekyll-theme-time-machine"
gem "jekyll-titles-from-headings"

# Plugins
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-readme-index"
  gem "jekyll-relative-links"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.0", :install_if => Gem.win_platform?

# kramdown v2 ships without the gfm parser by default. If you're using kramdown v1, comment out this line.
gem "kramdown-parser-gfm"

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
