require 'yamllint/rake_task'
require 'rake/clean'

CLEAN.include("./docs/*")
CLOBBER.include("./docs/*")

YamlLint::RakeTask.new do |t|
    t.paths = %w(
      _i18n/**/*.yml
    )
end

desc "build HTML from jekyll files for local."
task :build => :clean do
  sh "jekyll build"
end

desc "build HTML from jekyll files for production."
task :build_production => :clean do
  sh "env JEKYLL_ENV=production jekyll build"
end

desc "push files to origin/master."
task :push do
  sh "git push origin master"
end

desc "fetch and merge files from upstream."
task :pull_from_upstream do
  sh "git fetch upstream"
  sh "git merge upstream/master"
end
