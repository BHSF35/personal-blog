source "https://rubygems.org"

# 使用GitHub Pages gem，它会自动管理Jekyll和插件版本
gem "github-pages", group: :jekyll_plugins

# 额外插件
group :jekyll_plugins do
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
