require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'
require 'rake/dsl_definition'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "qurecode"
  gem.homepage = "http://github.com/yeti-media/qurecode"
  gem.license = "MIT"
  gem.description = "QRCode generator"
  gem.summary = "QRCode generator"
  gem.author = "Nicolas Santa"
  gem.email = "nicolas55ar@gmail.com"

  # Dependencies in Gemfile.
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['specs/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = 'specs/**/*_spec.rb'
  spec.rcov = true
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "anki-impo"

  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
