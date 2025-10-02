# Database Design Docs

> [!IMPORTANT]
> The database schema versioning system, is completely separate from the app versioning system. 
> And both has no co-relation at all. But both works hand in hand.

In this directory, You will find the general structure & format in which app stores users data.
Also you will, find different schema of database that app uses.

This docs will be especially useful if you want to extend passcodes app functionaltity. 
or build your custom backend for passcodes app. (currently we don't support custom backend.. but, we will soon do so..)

---

## Focus

> [!NOTE]
> Some feature might not be supported in SQLite & some might be specific to some type sql database.
>
> But as a developer we will try our best to abstract away database concept (from front-end) as much as possible by separating database functionality in a separate module. 
> and front-end will just call as simple as method like `savePassword()` or `loadPassword()` or something along that lines... to communicate with database...
>
> By, This way, app will stay most customizible & extensible.. And it won;t matter to frontend wether the app make a api request to your backend,
> or just store passwords in local storage.

We will here talk more in terms of sqlite and room framework for database. But mostly all of the concepts, sqlite support are fundemental to sql itself 
And Thus, they are support in most SQL databases out there. If you are planning to use monogodb or something in backend that you want to integrate with passcodes,
Then you might need to know SQL to some level and then you read this docs and translate this stuff into monogodb or any other db you use in custom backend (if possible)..

---

## List Of Databases

- Master Database [(master.db)](master.db)

## Tips & Recommendation

[Deep Guide](deep-guide.md)

XXXXX COMING SOON XXXXX

## How Write Migration / Docs / Test In CodeBase

Docs Template:- [template-docs](template-docs.md)

