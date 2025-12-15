# Master Database (master.db)

**Database**: SQLite(`master.db`)

It is a database where user info is stored. It schema changes often between the app versions, based on changes in feature requirements. 
Here, In this section you will find, all the version of database schema & will also find info about, how we adopted to the new schema.

| Version Name  | Introduce From    | Where Upto     |
| ------------- | ----------------- | -------------- |
| [dev](dev.md) | under development | ---            |
| [v1](v1.md)   | v1.0.0            | latest         |
| [v0](v0.md)   | v0.1.0            | v0.1.0         |

## Setup SQL

```sql
BEGIN TRANSACTION;

-- Create Master DB
CREATE DATABASE IF NOT EXISTS `master`;

COMMIT;

-- Activate Master DB
USE `master`;
```

## Revert SQL

```sql
BEGIN TRANSACTION;

-- Delete Master DB
DROP DATABASE IF EXISTS `master`;

COMMIT;
```

