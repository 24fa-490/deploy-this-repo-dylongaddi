# Starter Pack for using PostgreSQL with Svelte and SvelteKit
To install PostgreSQL on WSL (ie. Ubuntu):

Open your WSL terminal (ie. Ubuntu).
Update your Ubuntu packages: sudo apt update
Once the packages have updated, install PostgreSQL (and the -contrib package which has some helpful utilities) with: sudo apt install postgresql postgresql-contrib
Confirm installation and get the version number: psql --version
There are 3 commands you need to know once PostgreSQL is installed:

sudo service postgresql status for checking the status of your database.
sudo service postgresql start to start running your database.
sudo service postgresql stop to stop running your database.
The default admin user, postgres, needs a password assigned in order to connect to a database. To set a password:

Enter the command: sudo passwd postgres
You will get a prompt to enter your new password.
Close and reopen your terminal.
To run PostgreSQL with psql shell:

Start your postgres service: sudo service postgresql start
Connect to the postgres service and open the psql shell: sudo -u postgres psql
Once you have successfully entered the psql shell, you will see your command line change to look like this: postgres=#

 Note

Alternatively, you can open the psql shell by switching to the postgres user with: su - postgres and then entering the command: psql.

To exit postgres=# enter: \q or use the shortcut key: Ctrl+D

To see what user accounts have been created on your PostgreSQL installation, use from your WSL terminal: psql --command="\du" ...or just \du if you have the psql shell open. This command will display columns: Account User Name, List of Roles Attributes, and Member of role group(s). To exit back to the command line, enter: q.

For more about working with PostgreSQL databases, see the PostgreSQL docs.

To work with PostgreSQL databases in VS Code, try the PostgreSQL extension.

This info is taken from:
<https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-database#install-postgresql>

## uses 'postgres' npm package


# running:

1. git clone this

2. Install PostgreSQL on your computer, or sign up for a hosted instance

3. Create a database (e.g., 'containers')

4. Open a PSQL window and paste in the schema (from ```schema.sql```) in it.
   * If you are exporting a SQLite3 DB, you need to tweak it before it will work.

5. create ```.env``` file with contents ```PGCONNECT=postgres://bjmckenz@localhost:5432/containers``` in the project root (NOT inside SRC)
   * Substitute at least your name, and perhaps where your DB is installed.

5.5. I recommend installing the "PostgreSQL" VSCode extension by Weijan Chen so you can investigate the DB.

6. npm install

7. npm run dev

*Comments and feedback welcome!*

# Where am I deployed?

<enter your URL here>
