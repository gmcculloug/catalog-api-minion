begin
  require 'bundler/setup'
rescue LoadError
  puts 'You must `gem install bundler` and `bundle install` to run rake tasks'
end

require "rspec/core/rake_task"

Dir.glob("lib/tasks/*.rake") .each {|f| import f}

# Spec related rake tasks
RSpec::Core::RakeTask.new(:spec)

namespace :spec do
  task :initialize do
    ENV["RAILS_ENV"] ||= "test"
  end
end

task default: :spec
