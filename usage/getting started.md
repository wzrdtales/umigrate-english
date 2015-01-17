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

    $ umigrate dump

