source 'http://rubygems.org'

gemspec

group :development, :test do
  gem 'activerecord-jdbcmysql-adapter', platform: :jruby
  gem 'activerecord-jdbcpostgresql-adapter', platform: :jruby
  gem 'activerecord-jdbcsqlite3-adapter', platform: :jruby
  gem 'mysql2', platform: [:ruby, :mswin, :mingw]
  gem 'pg', platform: [:ruby, :mswin, :mingw]
  gem 'sqlite3', platform: [:ruby, :mswin, :mingw]
end


ar_version = ENV['ACTIVE_RECORD_VERSION']
ar_version = case ar_version
               when 'master' then {github: 'rails'}
               when String   then "~> #{ar_version}"
             end

mo_version = ENV['MONGOID_VERSION']
mo_version = case mo_version
               when 'master' then {github: 'mongoid'}
               when String   then "~> #{mo_version}"
             end

gem 'activerecord', ar_version if ar_version
gem 'mongoid',      mo_version if mo_version
