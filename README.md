# CMS for Zambia Superleague Website

## Installation

Chose the following options while the installation:

```bash 
npx strapi new superleague-strapi
? Choose your installation type Custom (manual settings)
? Choose your default database client mongo
? Database name: superleague-strapi
? Host: 127.0.0.1
? +srv connection: false
? Port (It will be ignored if you enable +srv): 27017
? Username: 
? Password: 
? Authentication database (Maybe "admin" or blank): 
? Enable SSL connection: No
```

## Check database

For testing check wheater there is a content type in the database: `http://localhost:1337/admin`. If not create one, for example: **standinds** with an integer field: **rank**.
And dataset and check the on the terminal if the data can be found:

```bash
$ mongo
>  show dbs
superleague-stapi         0.000GB
> use superleague-stapi
> show collections
standings
> db.standings.find()
{ "_id" : ObjectId("5e12da1912cc602bf3d2c4da"), "rank" : 1, "createdAt" : ISODate("2020-01-06T06:56:25.436Z"), "updatedAt" : ISODate("2020-01-06T06:56:25.436Z"), "__v" : 0 }
> exit
```
