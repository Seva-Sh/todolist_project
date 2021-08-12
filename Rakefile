require "rake/testtask"
require 'find'
require "bundler/gem_tasks"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end 

desc 'Run tests'
task :default => :test

desc 'Display inventory of all files'
task :inventory do
  Find.find('.') do |name|
    next if name.include?('/.')
    puts name if File.file?(name)
  end 
  # pth = "/home/seva/test_dir/todolist_project/"

  # Find.find(pth) do |path|
  #   path.delete_prefix!(pth)
  #   if path[0] != '.'
  #     if File.file?(path)
  #       puts path.gsub(/^.+\//, '') 
  #     end 
  #   end 
  # end 
end


Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end 