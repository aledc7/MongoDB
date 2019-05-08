# MongoDB
This repo contain the minimal information will able to you for a manage MongoDB Database.


- [x] aledc.com
- [x] MongoDB


### Get Started


The __How To__ install MongoDB will not be treated here, but surely you know how find this information ;)



*  How to show the current Database

```
db
```

* How to List all Databases

```
show databases
```


* How to USE a Database

```
use database_name
```

* How to CREATE a database

```
# is identical to USE, because if the DB doesn't exist, mongodb it will create automatically
use database_name
```

* Collection 

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


## How to Insert Data


```
insert()
```



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
        "name": "john doe", 
        "Website": "not found",
        "location": "Argentina"
      }
])
```


