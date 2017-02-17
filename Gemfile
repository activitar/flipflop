source "https://rubygems.org"
gemspec

gem "bootstrap", "= 4.0.0.alpha6"

group :test do
  version = ENV["RAILS_VERSION"] || "master"
  if version == "master"
    gem "rails", github: "rails/rails"
    gem "arel", github: "rails/arel"
  else
    gem "rails", "~> #{version}.0"
  end

  gem "sqlite3", ">= 1.3", platform: :ruby
  gem "fakeredis"
  gem "activerecord-jdbcsqlite3-adapter", platform: :jruby
  gem "minitest", ">= 4.2"
  gem "capybara", ">= 2.6"

  # Nokogiri 1.7+ requires Ruby 2.1.
  gem "nokogiri", "< 1.7"

  if ENV["RAILS_VERSION"] == "4.0"
    gem "minitest-rails", platform: :jruby
  end
end
