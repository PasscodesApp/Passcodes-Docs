# DEEP GUIDE

## How Room Libaray Handle Migration (Abstrat Understanding)

Room internally use a table in database called `room_master_table`, Inside it stores hash and id to track the version of database migration.

XXXXX Deep Explination Will Avaliable Soon XXXXX

## Database Guide (External Backend Developers)

We highly recommend using `PostgresSQL` as nowdays it a standard use by many companys.. It also has all features VectorDB, JsonDB and all fancy things...
But above all it is very extensive.. and has large community in my opionion. So, go with it.. It will also easy to apply this docs if use Postrgess SQL..

But you use any other db for that matter. like `MONGODB`, `MYSQL`, OR `may be pure binary files` to store data. 
because our app just shared the data with you, that user want to save and remember.. and it responsiblity of your backend to save it and give back,
when user through our app.. our app is just, a well client for user that they can just talk too...

Anyways, what ever you use, the database design docs will be your friend, helping you get idea of, how we structure the data and 
what data might your backend get from app that need to be store. If use sql database then no worry you use that stuff (inside docs) directly..
Otherwise there might little bit of work that you need to do.

Also don;t forget if you create custom backend always check app version, api version, database version... and make sure there is compatability.. 
and they go hand in hand with significant configuration, because our app changes often which mean your backend also need to change. 
And handle newer versions. and data that app provides your backend on api calls.

## Migration Handling Guide (External Backend Developers)

XXXXX WILL BE AVALIABLE SOON XXXXX

