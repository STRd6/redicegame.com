task :default => [:build]

task :build do
  sh "bundle exec middleman build"
end

task :update_ghpages_dir do
  sh "cd build && git pull"
end

task :deploy => [:update_ghpages_dir, :build] do
  sh "cd build && git ci -am `emoji` && git push"
end
