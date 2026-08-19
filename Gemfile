source "https://rubygems.org"

# Jekyll 4 rather than the `github-pages` gem: that gem pins Jekyll 3.9, which
# requires stdlib gems (csv, bigdecimal) that Ruby 3.4+ no longer bundles.
# Deployment goes through .github/workflows/jekyll.yml so production uses these
# same versions instead of GitHub's legacy Jekyll 3 builder.
gem "jekyll", "~> 4.4"
gem "minima"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
end

# No longer bundled with Ruby 3.0+, but Jekyll's dev server needs it.
gem "webrick"

platforms :windows do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
  # Native directory watching, so --livereload doesn't fall back to polling.
  gem "wdm", ">= 0.1.0"
end
