namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to the database'
  task migrate: :environment do
    Student.create_table
  end
  
  desc 'require environment before migrating'
  task :environment do
    require_relative './config/environment'
  end

  desc 'Seeding information to the terminal'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

desc 'require environment before migrating'
task :environment do
  require_relative './config/environment'
end
