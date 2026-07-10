source "https://rubygems.org"

gem "csv"
gem "bigdecimal"

# Theme
gem "jekyll-include-cache", group: :jekyll_plugins

# GitHub Pages configuration
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Windows and JRuby do not include zoneinfo files
platforms :windows, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Faster directory watching on Windows
gem "wdm", "~> 0.2.0", install_if: Gem.win_platform?

# JRuby compatibility
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]