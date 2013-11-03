task :default => [:install]

desc 'Setup subrepository'
task :install do
  system 'git submodule update --init'
end

# Usage:
#
#     rake wordpress_update[3.7.1]
#
desc 'Update Wordpress'
task :wordpress_update, :version do |t, args|
  puts args[:version]
  commands = [
    'git pull',
    'cd wordpress',
    'git checkout master',
    'git fetch --tags',
    "git checkout #{args[:version]}",
    'cd ..',
    'git add wordpress',
    "git commit -m 'Update Wordpress to #{args[:version]}'",
    'git push',
  ]

  system commands.join(' && ')
end