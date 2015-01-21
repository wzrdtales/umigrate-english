# Configuring database.json

```json
{
   "dev": {
      "driver": "mysql",
      "altDriver": "mariasql",
      "host": "localhost",
      "user": "root",
      "password": "root",
      "database": "test",
      "multiStatements": true,
      "template": "db-migrate",
      "filestring": "%action%_%filename%.js",
      "primary": true,
      "beautifier": "js-beautify",
      "beautifier_options":
      {
         "indent_size": 4,
         "indent_char": " ",
         "indent_with_tabs": false,
         "preserve_newlines": true,
         "max_preserve_newlines": 10,
         "space_in_paren": true,
         "e4x": false,
         "jslint_happy": true,
         "brace_style": "expand",
         "keep_array_indentation": false,
         "keep_function_indentation": false,
         "eval_code": false,
         "unescape_strings": false,
         "wrap_line_length": 0,
         "break_chained_methods": false
      },
      "db_persist": false
   }
}
```

The configuration above contains some parameters, which are self exaplained
or which have its own documentation in their own projects. E.g. js-beautify.

The first level defines the environment (dev, prod, test), the second level
contains all configuration parameters.

### altDriver

This configuration option was added because db-migrate use the driver option
and we wan't to use own drivers. If altDriver is obmitted umigrate trys to find
a driver that matches the `driver` option.

### primary

If this option is set to true, some templates will create PRIMARIES within the
table creation, instead of separating them to the indizies creation.

### template

This option allows you to change the used template which generate the output.
To include an external template written by someone refer to 
[this](http://umigrate.readthedocs.org/en/latest/features/#external-drivers-templates).

### filestring

This option lets you modify the format of the file that umigrate will write to.

### driver

This option allows you to change the used driver which fetches the information about
the schema and translates native types to generalized types.
To include an external driver written by somene refer to
[this](http://umigrate.readthedocs.org/en/latest/features/#external-drivers-templates).

### db_persist

This option allows you to specify wether the the diff database should persist or should be
rolled back.
This is useful if you want to edit the migration files by hand and the diff database will
be created from the start, while persisting will be in most cases faster.
