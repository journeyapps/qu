source "http://rubygems.org"
gemspec :name => 'qu'

Dir['qu-*.gemspec'].each do |gemspec|
  plugin = gemspec.scan(/qu-(.*)\.gemspec/).flatten.first
  gemspec(:name => "qu-#{plugin}", :development_group => plugin)
end

group :test do
  gem 'activesupport', :require => false
  gem 'statsd-ruby', '~> 1.2.1', :require => false
  gem 'rake', '< 11.0' # rspec-core <3.4.4 uses last_comment method which has been removed from Rake 11.0.1
  gem "rspec", "~> 2.14.1"
end
