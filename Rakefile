desc "Deploys to s3"
task :deploy do
  puts `middleman build`
  puts `cd build && aws s3 sync . s3://letteringbyhally.com --acl public-read`
end

task :default => :deploy
