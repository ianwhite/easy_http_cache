require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Run tests for Easy HTTP Cache.'
Rake::TestTask.new(:test) do |t|
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for Easy HTTP Cache.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Easy HTTP Cache'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('MIT-LICENSE')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = "easy_http_cache"
    s.version = "2.2"
    s.summary = "Allows Rails applications to use HTTP cache specifications easily."
    s.email = "contact@plataformatec.com.br"
    s.homepage = "http://github.com/josevalim/easy_http_cache"
    s.description = "Allows Rails applications to use HTTP cache specifications easily."
    s.authors = ['José Valim']
    s.files =  FileList["[A-Z]*", "lib/**/*", "init.rb"]
  end

  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler, or one of its dependencies, is not available. Install it with: sudo gem install jeweler"
end