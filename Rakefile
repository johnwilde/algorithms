require 'rake'
require 'rake/rdoctask'

# get the c specs running
require 'echoe'
require "rake/clean"
OBJ = FileList['**/*.rbc']
CLEAN.include(OBJ)

Echoe.new('grosser-algorithms') do |p|
  p.author               = 'Kanwei Li'
  p.email                = 'kanwei@gmail.com'
  p.summary              = 'A library of algorithms and containers.'
  p.url                  = 'http://rubyforge.org/projects/algorithms/'
  p.version              = File.read('VERSION').strip
  p.runtime_dependencies = []
end

desc 'Generate documentation for the userstamp plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.title    = 'Algorithms'
  rdoc.rdoc_dir = 'rdoc'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.markdown', 'History.txt')
  rdoc.rdoc_files.include('lib/**/*.rb')
end