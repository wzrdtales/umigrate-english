# Template creation

You want to create your own template? You don't need to directly contribute
to the project. You can require them directly in the 
[database.json config](http://umigrate.readthedocs.org/en/latest/features/#external-drivers-templates).

There are two ways, to use your own templates.

# Global deploy

You can create a template and make it available for everyone, by publishing it 
via npm.

You need to follow the name convention `umigrate-yourNameHere`.

# Local deploy

You don't need to publish your template, instead see the non global configuration
at the [features](http://umigrate.readthedocs.org/en/latest/features/)

## Base Template

You need to inherit from the following interface, or at least you need to 
provide all functions available.

To require the base template, you need to do the following:

    $ npm install umigrate-template-basedriver --save

After this you can require this base template and inherit from it via `util`.