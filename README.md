# MongoDB
This repo contain the minimal information will able to you for a manage MongoDB Database.


- [x] aledc.com
- [x] MongoDB


## Get Started


The __How To__ install MongoDB will not be treated here, but surely you know how find this information ;)



###  How to show the current Database

```
db
```

### How to List all Databases

```
show databases
```


###  How to USE a Database

```
use database_name
```
### How to CREATE a database

```
# is identical to USE, because if the DB doesn't exist, mongodb it will create automatically
use database_name
```

### Collection 

Collections is as a table is for SQL database...  yes... the comparison is valid :)


* How to Create a Collection

There are three ways to creare a collection. 

1. by insert data into the collection:
```
 mydb.colection_name.insert({"name": "Alejandro", "lastname" : De Castro, "location": "New York"})
```
2. by creating a non-capped collection:
```
 mydb.createCollection("colection_name")
```
3. by creating a capped collection:
```
mydb.createCollection("myOtherCollection", {capped : true, size : 512, max : 2})
```

A “capped collection” has a maximum document count that prevents Overflowing Documents.

In the exaple above i put a size of 512MB and a maximum of 2 documents.


### How to Insert Data




insertOne()
```
mydb.myCollection.insertOne(i
      {
       "name": "Alejandro", 
       "webpage": aledc.com
      }
)

```

insertMany()
```
mydb.myCollection.insertMany([
      {
        "name": "Alejandro", 
        "website": "aledc.com"
      },
      {
        "name": "Gary Wallis", 
        "website": "unxs.io"
      },
    
      {
        "name": "Abel Ranni", 
        "website": "ingenea.com.ar",
        "location": "Argentina"
      },
      {
        "name": "Jerrod Kuerth", 
        "website": "https://sulvo.com",
        "location": "New York"
      }      
      
])
```


insert()
```
is identical to insertMany()
```


### how to get Data



This is te basic way to querying Data
```
mydb.myCollection.find()
```

even you can add parameters, like ,pretty() for view the result as a Json aspect.  :)
```
mydb.myCollection.find().pretty()
```

### Automatic ID

when you insert a document in MongoDB, this automatically adds an **_id** field which uniquely identifies each document.

### how to HIDE the id
```
mydb.myCollection.find({}, _id: 0 ).pretty()
```

### how to FILTER data

```
mydb.myCollection.find(
 {
   name: "Alejandro"
 }
)
```
Of course, the indentation is optional, this isn't Python  ;)

here is another similar example without indentation:
```
mydb.myCollection.find({name: "Alejandro"})
```

### More ways to filter

$lt  (less than)
$gt (greater than)
$lte (less than or equal to)
$gte (greater than or equal to)
$ne (not equal)
```
mydb.myCollection.fid({age : {$lt: 7}})
```



### How to Update Documents

```
mydb.myCollection.update({name : "AleDC"}, {$set: {name: "Alejandro De Castro"}});
```

### how to remove a property
```
mydb.myCollection.update({name: "navindu"}, {$unset: age});
```

### how to delete a document
```
mydb.myCollection.remove({name: "Alejandro"});
```

### how to remove a collection
```
mydb.myCollection.remove({});
```

if you need more data, here is de [oficial documentation](https://docs.mongodb.com/)

