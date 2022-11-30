In the used database we are creating the alternative in SQL of tables, they are the Collections.

For created collection we are using the following command:
```mongodb
db.createCollection("[collectionName]")
```
Example:
```mongodb
webstore> use webstores
switched to db webstores
webstores> show collections

webstores> db.createCollection("users")
{ ok: 1 }
webstores> db.createCollection("sellers")
{ ok: 1 }
webstores> show collections
sellers
users
webstores>
```
For delete collection we are using:
```mongodb
db.[CollectionName].drop()
```
Example:
```mongodb
webstores> show collections
products
sellers
users
webstores> db.products.drop()
true
webstores> show collections
sellers
users
webstores>
```

