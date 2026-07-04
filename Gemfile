source "https://rubygems.org"

# This installs the exact same Jekyll + plugin versions that GitHub Pages
# uses to build sites, so what you see locally matches what publishes.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed"
end

# Windows/JRuby compatibility (harmless to leave in on macOS/Linux)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
