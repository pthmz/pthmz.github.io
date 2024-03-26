source "https://rubygems.org"
# 嗨！在这里管理用于运行的 Jekyll 版本。
# 如果你想使用其它版本，可以在下面更改，保存此
# 文件并运行 `bundle install`。使用 `bundle exec` 运行 Jekyll，如下所示：
#
#     bundle exec jekyll serve
#
# 这有助于确保使用的是正确的 Jekyll 版本。
# 愉快地使用 Jekyll！
gem "jekyll", "~> 4.3.3"
# 这是新建 Jekyll 站点的默认主题。你可以更改为任何你喜欢的主题。
gem "minima", "~> 2.5"
# 如果想使用 GitHub Pages，请移除上面“gem “jekyll””并
# 取消下面这行的注释。要更新，运行 `bundle update github-pages`。
# gem "github-pages", group: :jekyll_plugins
# 如果有任何插件，请放在这里！
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Windows 和 JRuby 不包括时区信息文件，因此 bundler tzinfo-data gem
# 和关联库。
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Windows 上监视目录的性能增强器
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# 在 JRuby 构建上将 `http_parser.rb` gem 锁定到 `v0.6.x`，因为新版 gem 没有 Java 对应项。
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]