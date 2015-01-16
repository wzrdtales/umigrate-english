# Template creation

You want to create your own template? You don't need to directly contribute
to the project. You can require them directly in the database.json config.

## Base Template

You can inherit from the following template, which is also found here
/lib/template/base.js

```javascript
function BaseTemplate()
{}

BaseTemplate.prototype = {

    table: function ( table, columns, drop )
    {
        throw new Error( 'not implemented' );
    },

    columns: function ( table, columns, drop )
    {
        throw new Error( 'not implemented' );
    },

    changeKeys: function ( table, keys, drop, index )
    {
        log.verbose( 'not implemented' );
    },

    keys: function ( table, keys, drop, index )
    {
        log.verbose( 'not implemented' );
    },

    engine: function ( table, engines, drop )
    {
        log.verbose( 'not implemented' );
    }
};

module.exports = BaseTemplate;
```