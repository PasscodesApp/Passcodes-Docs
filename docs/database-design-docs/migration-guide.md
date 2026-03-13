# Database Migration Guide & Contribution Rules

This document defines the **official workflow and rules** for creating, testing, and merging database migrations in the Passcodes project.

## Why This Rules Exists?

These rules exist to **protect user data (sensitive data)** and ensure the database schema evolves safely.

- [Migration Vidoe of "`Theo - t3․gg`"](https://youtu.be/jeWrbAiA1D0)


## Overall Migration Rules / Migration Process

1. when you wanna change the database scheme of passcodes, you have to before time, draft a new P.R. of the new schema in our docs and need to await for it's merge in our doc's..

2. your new P.R. (to docs repository) should draft a new database scheme file, that should ideal be consistent with exist database docs. like it should migartion sql and all..

3. when your docs changes P.R. merge in our docs repository. which mean your scheme will be visible in our docs host using github pages online. then only you can even start write code in codebase (passcodes app repository) releated to migration.

4. after, the code changes you will likely draft a PR in app repository. please mention and link the schmema migration docs (github pages) and schema pr that was draft on docs repository. 

5. ask for review on PR from the offical maintainers.

**Summary**: `Pr-docs` -> `Code-changes`.

---

## Migration Philosophy

The Passcodes database stores **user credentials and sensitive information**.
Any mistake in migration logic can result in **permanent user data loss**.

Because of this, **database migrations are treated as critical changes** and must follow a strict process.

No migration should be merged unless all rules in this document are satisfied. (ideally)

---

## Migration Development Workflow

Every schema change must follow the workflow below.

```
Update Documentation
↓
Review Schema Change
↓
Merge The Documentation Changes
↓
Implement Room Migration
↓
Test Migration Locally
↓
Submit Pull Request
↓
Migration Review
↓
Merge Code Changes
```

Documentation is always the **source of truth**.

---

## Pull Request Requirements

A pull request introducing a migration must include:

```
[ ] Updated schema documentation (a link to it)
[ ] Room migration implementation
[ ] Migration testcases
```

Pull requests missing any of the above requirements should not be merged.

---

## Responsibility

Database migrations directly impact **all existing users** of the application.

Contributors must treat migrations with extreme care and follow these rules strictly.

Protecting user data is the **highest priority** when evolving the database schema.

---

## Mandatory Migration Rules

The following rules are **strict requirements** for any database schema change.

Pull requests that violate these rules **must not be merged**.

---

### Rule 1 — Documentation Must Be Updated First

Database schema documentation **must be updated before any code implementation**.

The required order is:

```
1. Update database documentation
2. Define schema changes
3. Write migration SQL
4. Implement Room migration in code
```

This ensures that the documentation remains the **canonical definition of the schema**.

Pull requests that modify database code without updating documentation **will be rejected**.

---

### Rule 2 — Schema Must Be Clearly Versioned

Each schema version must include:

* schema description
* setup SQL
* migration SQL
* revert SQL
* change summary

This ensures that the database history remains **auditable and reproducible**.

---

### Rule 3 — All Migrations Must Be Implemented Using Room

Every schema change must include a (`single standalone`) corresponding `"manual migration"` using
Android Room.

Example:

```
Migration(1, 2)
Migration(2, 3)
```

"Jump migration" (Migration(1, 5)) supported by room library must be avoid unless needed explictly. (like for performance optimization)

Room must be responsible for applying migrations during database upgrades.

Manual schema modifications outside Room migrations are **not allowed**.

---

### Rule 4 — Destructive Migrations Are Forbidden

The following configuration must **never be used in production builds**:

Also, the follow code should never be merged in main.

```kotlin
fallbackToDestructiveMigration()
```

Destructive migrations delete the database and result in **total user data loss**.

Any pull request containing destructive migration logic will be rejected.

---

### Rule 5 — Existing User Data Must Be Preserved

Migrations must guarantee that **all existing user data remains intact**.

The following must never occur during migration:

* deletion of user passwords
* unintended overwriting of fields
* dropping tables without copying data

If a table must be rebuilt, the following pattern must be used:

```
CREATE new_table
COPY existing data
DROP old_table
RENAME new_table
```

All relevant columns must be preserved during the copy step.

---

### Rule 6 — Migrations Must Be Deterministic

Migration behavior must be predictable and independent of device state.

Migrations must **not depend on**:

* device configuration
* application state
* network calls
* runtime conditions

Migration logic must rely **only on the existing database contents**.

---

### Rule 7 — Migration Logic Is Immutable After Release (Even after merge in main branch)

Once a database version is released to users, the migration associated with that version **must never be modified**.

If improvements are required later, a **new migration version must be introduced**.

Example:

```
v1 → v2 migration (immutable)
v2 → v3 migration (new improvements)
```

This guarantees consistent upgrade paths across all devices.

---

### Rule 8 — Migrations Must Remain Simple

Database migrations should remain **as simple as possible**.

Also the sql used must optimize for readablity rather then doing three differnt concern things in single sql query.

Preferred operations:

```
ADD COLUMN
CREATE TABLE
CREATE INDEX
```

Complex transformations should be avoided unless absolutely necessary.

Simple migrations reduce the risk of errors and improve reliability.

---

## Migration Testing Workflow

All migrations must be tested before submission.

Testing simulates a real user upgrading the application.

#### Testing Flow

```
Install old database version
↓
Insert test records
↓
Upgrade to new database version
↓
Run migration
↓
Verify schema
↓
Verify data integrity
```

---

### Required Verification

After migration:

1. The application must start successfully.
2. The database schema must match the expected version.
3. Existing user records must still exist.
4. New schema fields must function correctly.

Example test record:

```
domain: github.com
username: example_user
password: example_password
notes: test account
```

The record must remain accessible after migration.

---

### Edge Case Testing

The following cases should also be verified:

- multiple records
- empty fields
- long text values
- special characters
- NULL values (when allowed)

This helps detect hidden migration issues.

---
