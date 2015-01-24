# Driver creation

You want to create your own driver? You don't need to directly contribute
to the project. You can require them directly in the 
[database.json config](http://umigrate.readthedocs.org/en/latest/features/#external-drivers-templates).

There are two ways, to use your own drivers.

# Global deploy

You can create a driver and make it available for everyone, by publishing it 
via npm.

You need to follow the name convention `umigrate-yourNameHere`.

# Local deploy

You don't need to publish your driver, instead see the non global configuration
at the [features](http://umigrate.readthedocs.org/en/latest/features/)

## Base Driver

You need to inherit from the following interface, or at least you need to 
provide all functions available.

To require the base driver, you need to do the following:

    $ npm install umigrate-db-basedriver --save

After this you can require this base driver and inherit from it via `util`.