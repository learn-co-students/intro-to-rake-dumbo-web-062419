desc 'initialize the environment'
task :environment do
	require_relative "./config/environment"
end

desc 'initialize the console'
task :console do
	irb
end

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
	desc 'will perform a migration'
	task :migrate => :environment do
		Student.create_table
	end

	desc 'will seed the database with data'
	task :seed => :environment do
		require_relative './db/seeds.rb'
	end
end