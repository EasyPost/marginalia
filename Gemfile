source "https://rubygems.org"

gemspec

version = ENV["RAILS_VERSION"] || "4.2.0"

gem 'mysql'
if "4.2.5" > version
  gem 'mysql2', '~> 0.3.13'
else
  gem 'mysql2', '>= 0.3.13', '< 0.5'
end
gem 'pg', '~> 0.15'
gem 'sqlite3'

rails = case version
when "master"
  {:github => "rails/rails"}
else
  "~> #{version}"
end

gem "rails", rails

if ENV["TEST_RAILS_API"] == "true"
  gem "rails-api", "~> 0.2.1"
end
