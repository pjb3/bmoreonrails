load 'deploy' if respond_to?(:namespace) # cap2 differentiator


set :application, "bmoreonrails"
set :scm, "git"
set :repository, "git@github.com:jjulian/bmoreonrails.git"
set :branch, "gh-pages"

role :web, "67.207.150.229"
set :user, "www-data"
set :use_sudo, false
set :deploy_to, "/var/www/bmoreonrails"

# custom
set :stay_with_a_local_root, "/var/www/stay-with-a-local/public"

namespace :deploy do
   task :start do ; end
   task :stop do ; end
   task :restart do ; end
   task :migrate do ; end
   task :migrations do ; end
   task :cold do ; end
end

task :symlink_stay_with_a_local do
  run "ln -s #{stay_with_a_local_root} #{release_path}/stay-with-a-local"
end

after :deploy, :symlink_stay_with_a_local