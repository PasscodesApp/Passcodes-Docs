In this directory, You will find the general structure & format in which app stores users data. Also you will you will find different schema of database.

> Some feature are not supported in SQLite and some might be specific to some database. but as a developer we will try our best to abstract away database concept (from front-end) as much as possible by separating database functionality in a separate module. and front-end will just call as simple as method like `savePassword()` or `loadPassword()` or something along that lines... to communicate with database...

> [!NOTE]
> Database schema versioning system is completely separate from the app versioning system.

## List Of Databases

- Master Database [(master.db)](database-design-docs/master.db/README.md)
