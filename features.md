# Multi-DB-Typing

Multi-DB-Typing means the automatic conversion of native types.
This will be essentially a functionality of the driver.

This feature is a dependency to the goal of cross compatibility between
different Databases.

The types needs to be converted like the following:

    VARCHAR(LENGTH)->TEXT(LENGTH)


# External Drivers/Templates

## Global

External Drivers and templates are required via the following configuration if 
they are global:

```json
{
    "dev": {
        "altDriver": "yourwishedumigratedriver",
        "template": "yourwishedumigratetemplate"
    }
}
```

This name gets automatically resolved to `umigrate-yourwishedumigratetemplate`.

**Also note:** To be able to require packages which are installed globally, 
you need to have your **NODE_PATH** defined.

## Non global

External Drivers and templates are required via the following configuration if 
they are not global:

```json
{
    "dev": {
        "altDriver": {
            "require": "yourwishedumigratedriver"
        },
        "template": {
            "require": "yourwishedumigratetemplate"
        }
    }
}
```