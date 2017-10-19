namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'prints hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end


namespace :db do
  desc 'migrates changes to your database'
  task :migrate => :environment do
    Student.create_table
    end

  desc 'creates environment dependency'
  task :environment do
  require_relative './config/environment'
  end

  desc 'seeds information to the databse'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'opens into a console with dummy data'
  task :console => environment do
    Pry.start
  end
end
