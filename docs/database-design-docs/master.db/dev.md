# Dev Schema

- **Used by**: `vX.X.X` => `latest`
- **Purpose**: Add URL features to appilcation

---

## Entire Database Schema (v2)

### Tables

| Tables      | Description                  |
| ----------- | ---------------------------- |
| `passwords` | For storing password entity. |

### Passwords Table (`passwords`)

| Fields       | Property | Constraints                | Description                                                                                             |
| ------------ | -------- | -------------------------- | ------------------------------------------------------------------------------------------------------- |
| `id`         | Integer  | PRIMARY KEY, AUTOINCREMENT | --                                                                                                      |
| `domain`     | Text     | NOT NULL                   | domain/platform name to which password enitity is associated with.                                      |
| `username`   | Text     | NOT NULL                   | username on that domain / platform. email can be even used as a value.                                  |
| `password`   | Text     | NOT NULL                   | password for that specfic username on that specfic domain / platform.                                   |
| `notes`      | Text     | ---                        | notes that you wanna take for that record. more like be some information about account on that platform |
| `url`        | Text     | ---                        | link to a platform/domain/website.. can be a application package name, uri, https:// url.               |
| `created_at` | Text     | DEFAULT CURRENT_TIMESTAMP  | --                                                                                                      |
| `updated_at` | Text     | DEFAULT CURRENT_TIMESTAMP  | --                                                                                                      |

---

## Setup SQL (v2)

```sql
BEGIN TRANSACTION;

CREATE TABLE IF NOT EXISTS `passwords` (
	`id` INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
	`domain` TEXT NOT NULL,
	`username` TEXT NOT NULL,
	`password` TEXT NOT NULL,
	`notes` TEXT,
    `url` TEXT,
	`created_at` TEXT DEFAULT CURRENT_TIMESTAMP,
	`updated_at` TEXT DEFAULT CURRENT_TIMESTAMP
);

COMMIT;
```

## Changes Made

- `notes` field/column is made nullable.
- a new `url` field is introduced for URL's.
