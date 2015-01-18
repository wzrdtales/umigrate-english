# General Usage

```shell
Usage: umigrate [up|down|create|dump] migrationName [options]

Options:
  --env, -e               The environment to run the migrations under (dev, test, prod).                      
  --migrations-dir, -m    The directory containing your migration files.                                        [default: "./migrations"]
  --count, -c             Max number of migrations to run.                                                    
  --dry-run               Prints the SQL but doesn't run it.                                                    [boolean]
  --force-exit            Forcibly exit the migration process on completion.                                    [boolean]  [default: false]
  --verbose, -v           Verbose mode.                                                                         [default: false]
  --version, -i           Print version info.                                                                   [boolean]
  --diffdb, -d            Specify manually a DataBase to diff.                                                
  --cross-compatible, -x  Dumper will run in compatible mode. By default everything generic keeps x-compatible  [default: false]
  --template, -t          Specify which tempĺate to use.                                                      
  --config                Location of the database.json file.                                                   [string]  [default: "./database.json"]
```

### Execute Dump

To dump your database you need first to configure your database config. If
you've done this, you can execute the following:

    $ umigrate dump

**Note:** Please notice, the user which is reading from your database needs
access to multiple databases. It's recommended to use a user with higher global
privileges, at least reading all databases as this user needs for example to 
read from the **mysql** and **information_schema** table if using **mysql** and 
also reading and writing to the diff database. 

**Important: Currently you need to create the `your_database_here_diff` manually
as this must be implemented to db-migrate. This is planned for future releases.**

Umigrate will now try to make a difference between `your_database_name` and 
`your_database_name_diff`. The `_diff` suffix gets appended automatically.
Alternatively you can append the command -d, to select the database whith which
umigrate will generate the difference.

    $ umigrate dump -d myChoosedDB

### Using Migrations

Please view the [documentation of db-migrate](https://github.com/kunklejr/node-db-migrate/)
for further information.