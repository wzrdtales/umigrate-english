## FAQ

 * Why did you decided to write another migrator?

Well I didn't decided to do this exactly, more then I wanted to create a Migration Helper instead of writing my own Migrator. I like the concept behind Migrations, but I hate it to do things twice. When I was working on any Database I already knew that I have to transfer my changes to the Migrations. Bad enough, but the true pain is to setup Migrations for an old project and transcribe the whole Schema.
There are several tools out there, that pretend to help me with this. But finally they just generated more pain, then before. This is the final reason I decided to work on a full featured Database Migration Helper, which will include in some later Releases a full featured Migrator itself. Probably still db-migrate, but feature complete. Hopefully...

 * Nothing happens when -x is used, why?

The option -x will probably become deprecated, as it has no functionality now and I'm not sure if I'm going to implement it. It is generally a product of an earlier design approach, which changed greatly while the development. I will review and revise this in near feature and then decide what to do.
This earlier design approach was to enable functionality that is currently not implemented, by enabling and disabling raw queries (and so disabling Database features) through -x. Later on I decided to not provide this step by step implementation with fallback to raw Queries.

 * Do you have plans for future releases?

Well..., yes. Just view the Roadmap. 

 * Should I really don't care about Migration Compatiblity when switching Database Engines?

It depends, if you're switching between a Database Engine that supports foreign keys and one that do not and of course all relations are implemented outside the Database, you don't need to care.
But if you switch between a Database Engine that supports functions and one that don't, you're probably screwed.
It's all about making the right decisions.


 * Do you hate RAW Queries?

No, I love them and prefer them in most cases over any Abstraction. There is nearly no case I could think of, where I would prefer to not use RAW Queries. This project is one of this special cases. You can't provide Cross Compatibility without providing generic functionality, that can be translated to the different Database Engines and its specifications.