Created database temporaly:
```mongodb
use webstore
```
For verify that we haven´t a created a database in mongo is with command `show dbs`
```mongodb
mongo> use webstore
switched to db webstore
webstore> show dbs
admin   40.00 KiB
config  96.00 KiB
local   72.00 KiB
webstore>
```
This happend because the database is "created" after insert data on the temporary database. In this case on "webstore"

For insert data in the database we are using the following command:
```mongodb
db.products.insert({"name":"laptop"})
```
Output
```mongodb
webstore> show dbs
admin   40.00 KiB
config  96.00 KiB
local   72.00 KiB
webstore> db.products.insertOne({"name":"laptop"})
{
  acknowledged: true,
  insertedId: ObjectId("63878594a611af964bcdc279")
}
webstore> show collections
products
webstore> show dbs
admin      40.00 KiB
config    108.00 KiB
local      72.00 KiB
webstore   40.00 KiB
webstore>
```
Delete database we are using, for verify the database that we are deleting use the comand `db`
```mongodb
webstore> db
webstore
webstore> db.dropDatabase()
{ ok: 1, dropped: 'webstore' }
webstore> show dbs
admin    40.00 KiB
config  108.00 KiB
local    72.00 KiB
```