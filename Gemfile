# Gemfile

source "https://rubygems.org"

# Specify the version of Jekyll to use
gem "jekyll", "~> 4.3"

# Specify your theme
gem "just-the-docs"

# A dependency for running a local server with Ruby 3+
gem "webrick", "~> 1.8"

# --- Keep the platform-specific gems below ---

# Windows and JRuby does not include zoneinfo files
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", ">= 0.2.0", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]