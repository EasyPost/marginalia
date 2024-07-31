source "https://rubygems.org"

gemspec

rails_version = ENV["RAILS_VERSION"] || "6.1.0"
if rails_version == "main"
  gem "rails", github: "rails/rails"
else
  gem "rails", "~> #{rails_version}"
end

# Different versions of Rails will depend on different versions
# of sqlite3. Defaulting to the version depended on by 6.1.0.
#
# @see https://github.com/rails/rails/blob/v6.1.0/Gemfile.lock#L615
sqlite3_version = ENV["SQLITE3_VERSION"] || "1.4.0"
gem "sqlite3", "~> #{sqlite3_version}"

gem "activerecord-trilogy-adapter", "~> 3.1"
