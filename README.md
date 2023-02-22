# mongo-db-crud-operations

Mongo db is a nosql data base

The folllowing are the crud operations in mongodb

```
C - CREATE
R - READ
U - UPDATE
D - DELETE
```

## Steps to **create** a schema using mongosh

1. create a **database** and under it create a **collection**
2. in the **mongosh** it will be initially ` >test `
3. so to change it to our db the folllowing command is used
` use dbname(db name is the name of ur db) `

4. Inorder to __insert/create a single record__ 
```javaScript
db.MobileFeature.insertOne({"mobileName" : "samsung",
  "mobileColour" : "blue",
  "mobileRam" : 256,
  "mobileOs" : "android"
})

once the schema is inserted an *_id which is ObjectId* is automatically created for each schema
```
5. Inorder to **insert multiple records** 
```javascript
```


6. The below command to **Read all the data**
` db.collectionname.find({}) `

To read data basing on specific value
`db.MobileFeature.find({"mobileOs":"androidOs"})`

7. Inorder to **update** the schema it contains two parts the first one is the value basing on which values will be updates and the second one is where using $set the values will be updated  
```javascript
db.MobileFeature.updateOne({ _id : ObjectId("63f5ed537083c56834f0a383")},
{
$set: {
  "mobileOs" : "androidOs"
}})
```

8. in order to update multiple records
```javascript
db.MobileFeature.updateMany(
{ _id : ObjectId("63f5ed537083c56834f0a383")},
{
$set: {
  "mobileOs" : "androidOs"
}},
{ _id : ObjectId("63f5ed537083c56834f0a384")},
{
$set: {
  "mobileColour" : "Blue"
}})
```


9. Delete a **single schema**
```javascript
db.MobileFeature.deleteOne({ _id : ObjectId("63f5ecc27083c56834f0a383")})
```

10. Delete **all schema**
```javascript
db.MobileFeature.deleteMany({})
```



















