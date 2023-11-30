source "https://rubygems.org"

gem "webrick"
gem "jekyll"

gem "kramdown-parser-gfm" if ENV["JEKYLL_VERSION"] == "~> 3.9"

gem 'wdm', '>= 0.1.0' if Gem.win_platform?
group :jekyll_plugins do
    gem "jekyll-paginate-v2"
    gem "jekyll-feed"
  end