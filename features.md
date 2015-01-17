# Multi-DB-Typing

Multi-DB-Typing means the automatic conversion of native types.
This will be essentially a functionality of the driver.

This feature is a dependency to the goal of cross compatibility between
different Databases.

The types needs to be converted like the following:

    VARCHAR(LENGTH)->TEXT(LENGTH)

# External Drivers/Templates

External Drivers and templates are required via the following configuration:

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