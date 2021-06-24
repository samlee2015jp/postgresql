# postgresql manual

Brew Package Manager

In your command-line run the following commands:

brew doctor
brew update
Installing

In your command-line run the command: brew install postgres

Run the command: ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents

Create two new aliases to start and stop your postgres server. They could look something like this:

     alias pg_start="brew services start postgresql"
     alias pg_stop="brew services stop postgresql"
     alias pg_restart="brew services restart postgresql"
Run the alias you just created: pg_start. Use this comment to start your database service.

alternatively, pg_stop stops your database service.
Run the command: createdb `whoami`

Connect to your postgres with the command: psql

brew reinstall readline - ONLY IF NEEDED

createuser -s postgres - fixes role "postgres" does not exist

Test with psql command

$ psql
psql (10.0)
Type "help" for help.

ibraheem=# 
Details

What is this ln command I ran in my Terminal?

from the man ln command

The ln utility creates a new directory entry (linked file) which has the same modes as the original file. It is useful for maintaining multiple copies of a file in many places at once without using up storage for the copies''; instead, a link points'' to the original copy. There are two types of links; hard links and symbolic links. How a link ``points'' to a file is one of the differences between a hard and symbolic link.
What is launchctl?

from the man launchctl command

launchctl interfaces with launchd to manage and inspect daemons, angents and XPC services.
Commands

Create database

createdb <database_name>
createdb mydjangoproject_development
List databases

psql -U postgres -l
Show tables in database

psql -U postgres -d <database_name>
psql -U postgres -d mydjangoproject_development
Drop database

dropdb <database_name>
dropdb mydjangoproject_development
Restart database

dropdb <database_name> && createdb <database_name>
dropdb mydjangoproject_development && createdb mydjangoproject_development
