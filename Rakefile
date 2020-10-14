require "html-proofer"

task :test do
  sh "bundle exec jekyll build -q"
  options = { :assume_extension => true, :empty_alt_ignore => true, :http_status_ignore => [400] }
  HTMLProofer.check_directory("./_site", options).run
end
