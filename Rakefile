require 'rake/testtask'
require 'find'

desc 'Say hello'
task :hello do
    puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List files'
task :files do
  Find.find('.') do |file|
  next if file.include?('/.')
  puts file if File.file?(file)
  end
end


