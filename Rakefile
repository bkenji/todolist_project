require 'rake/testtask'
require 'find'

require "bundler/gem_tasks"

desc 'Say Hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'List all visible files'
task :list_visible do
 Find.find('.') do |name| # the . here represents the current directory
  next if name.include?('/.')
  puts name if File.file?(name)
 end
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList["test/**/*_test.rb"]
end


