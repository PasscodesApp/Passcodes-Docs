# DEEP GUIDE

## How Room Libaray Handle Migration (Abstrat Understanding)

Room internally use a table in database called `room_master_table`, Inside it stores hash and id to track the version of database migration.

It then do some magically comparaion to tell which version the database is on. also, tell is there need for migration or not..

## Database Guide (External Backend Developers)

We highly recommend using `PostgresSQL` as nowdays it a standard, use by many companys.. It also has all features VectorDB, JsonDB and all sorts of fancy things...
But, above all it is very extensive.. and has large community in my opionion. So, go with it.. It will be also easy to apply, this docs if you use Postrgess SQL..

But you use any other db for that matter. like `MONGODB`, `MYSQL`, OR `may be pure binary files` to store data. 
because our app just shared the data with you, that user want to save and remember.. and it pure responsiblity of your backend to save it and give it back,
when user ask through our app.. our app, well in this case, would be just a client application for user, that they can just talk too for ease of use...

Anyways, whatever you use, the database design docs will be your friend, helping you though, to get an idea of, how we structure the data over here in passcodes and 
what (kind of) data your backend can expect to get from app that need to be store. If you use sql database, then no worry you use this stuff (docs) directly..
Otherwise there might be little bit of work that need to be done.

Also don;t forget if you create custom backend always check app version, api version, database version... and make sure they are compatability which each other.. 
Also, Ensure that the app version (passcodes), api version (your's) & database version (your's) system, go hand in hand, without any need for significant configuration, 
Because our app changes often, which mean your backend also need to adopt to it, to stay up-to-date and handle newer versions. 
So, that the data that app provides to your backend on api calls can be except by your app. Otherwise, your backend might panic and crash on new data.
Because our app send something your backend didn;t expected at glance.

## Migration Handling Guide (External Backend Developers)

> [!IMPORTANT]
> It is just to give you a idea, consider it as a guide and not as a hard written rule.

This by no mean come under passcodes, custom backend need to handle data on thier own and its purely thier responsiblity.
custom backend are responsible for implement a priesentent data storeage system... and thus, migration handle is also there responsiblity.
So, consider this as a guide. take inspiration from it. make what ever work for you..

With that said, Here are two ways we recommend, developers to achive database migration.

Firstly, despite any of two you use, you need a version system if wanna stay backward compatabile. otherwise, this migration guide is trash for you. 
because, if you wish not to stay backward compatible, then ofcourse fo ahead, shutdown your backend for sometime.
connect to db using client, make a change in schema (un-recoreded migration in production db which is significantly destructive), 
migrated old data to new schema and say sorry to users for the down time (and if unlucky, say sorry for data loss also).

> By backward compatablity, I mean, you want manual migration that has a full forward-backward compatabilty. which means you can apply or un-apply (revert) them any time.

Okay, you read this means you have version system and care for backward compatablity of your backend.

Here two ways you track migration,

1. Have a json file.

- Quick & Lazy Way + Ease-of-use.
- Require minimal efforts for setup.
- Venurable to human (developers) mistake.
- Customiziable & Extenisive. (it can be extend to remove its initial limitaions).

Make a json file to keep track of database version you are currently own. also write other essential infomation.
It can live into your project root directory can be also with deploy api.

```json
{
    "our-custom-db": {
        "version": 1,
        "last-migration": "2025-10-02T15:11:21Z",
        "is-production-db": true,
    },
    "our-test-cudtom-db": {
        "version": 3,
        "last-migration": "2025-10-02T15:11:21Z",
        "is-production-db": false,
    }
}
```

2. Have a dedicated table in db. (strongly recommended)

- Need Setup.
- Less venurable to human errors. much hard to go wrong.
- Database version can find in db itself.

You can have table called `migration_history`. and then use it to keep track of migration on database.

```sql
CREATE TABLE `migration_history` (
    `id` INTEGER PRIMARY KEY AUTOINCREMENT,
    `from` INTEGER NOT NULL,
    `to` INTEGER NOT NULL,
    `apply_at` DATE DEFAULT CURRENT_TIMESTAMP,
);
```

```sql
INSERT INTO `migration_history` (`from`, `to`) VALUES (1, 2);
```

```sql
SELECT `to` FROM `migration_history` SORT BY `apply_at` LIMIT 1;
```

