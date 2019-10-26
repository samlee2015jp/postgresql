learning postgresql

To migrate existing data from a previous major version of PostgreSQL run: brew postgresql-upgrade-database

To have launchd start postgresql now and restart at login: brew services start postgresql Or, if you don't want/need a background service you can just run: pg_ctl -D /usr/local/var/postgres start ==> Summary 🍺 /usr/local/Cellar/postgresql/11.5_1: 3,189 files, 36.4MB


The files belonging to this database system will be owned by user "Sam".
This user must also own the server process.

The database cluster will be initialized with locale "ja_JP.UTF-8".
The default database encoding has accordingly been set to "UTF8".
initdb: could not find suitable text search configuration for locale "ja_JP.UTF-8"
The default text search configuration will be set to "simple".

Data page checksums are disabled.

creating directory /usr/local/pgsql/data ... 

MacBook-Air:postgres Sam$ initdb -D /usr/local/var/postgres/data
The files belonging to this database system will be owned by user "Sam".
This user must also own the server process.

The database cluster will be initialized with locale "ja_JP.UTF-8".
The default database encoding has accordingly been set to "UTF8".
initdb: could not find suitable text search configuration for locale "ja_JP.UTF-8"
The default text search configuration will be set to "simple".

Data page checksums are disabled.

creating directory /usr/local/var/postgres/data ... ok
creating subdirectories ... ok
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default timezone ... Asia/Tokyo
selecting dynamic shared memory implementation ... posix
creating configuration files ... ok
running bootstrap script ... ok
performing post-bootstrap initialization ... ok
syncing data to disk ... ok

WARNING: enabling "trust" authentication for local connections
You can change this by editing pg_hba.conf or using the option -A, or
--auth-local and --auth-host, the next time you run initdb.

Success. You can now start the database server using:

    pg_ctl -D /usr/local/var/postgres/data -l logfile start
    
