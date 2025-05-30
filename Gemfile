source "https://rubygems.org"

# Jekyll核心
gem "jekyll", "~> 4.3.2"

# GitHub Pages兼容
gem "github-pages", "~> 228", group: :jekyll_plugins

# Jekyll插件
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows支持
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# 性能优化
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# 修复兼容性问题
gem "webrick", "~> 1.8"
