namespace :greeting do
desc 'wazzawazzawoo'
task :hello do
  puts "hello from Rake!"
end
desc 'hola'
task :hola do
  puts 'hola de Rake!'
end
end
namespace :db do
  desc 'add the environment task'
  task :environment do
      require_relative './config/environment'
    end
  desc 'migrate changes to your database'
  task :migrate => :environment do
      Student.create_table
    end
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end
desc 'pry it open'
task :console => :environment do
  Pry.start
end
