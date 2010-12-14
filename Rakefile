require 'rubygems'
gem 'hoe', '>= 2.1.0'
require 'hoe'
require 'fileutils'
require './lib/action_web_service'

Hoe.plugin :newgem
# Hoe.plugin :website
# Hoe.plugin :cucumberfeatures

# Generate all the Rake tasks
# Run 'rake -T' to see list of generated tasks (from gem root directory)
$hoe = Hoe.spec 'action_web_service' do
  self.developer 'Andrew Forward', 'andrew.forward@cenx.com'
  self.summary="Fork of datanoise-actionwebservice to enable plugin with Rails 2.3.8"
  self.post_install_message = 'PostInstall.txt'
  self.extra_deps         = [['rails','>= 2.3.0']]
end

require 'newgem/tasks'
Dir['tasks/**/*.rake'].each { |t| load t }

# TODO - want other tests/tasks run by default? Add them to the list
# remove_task :default
# task :default => [:spec, :features]
