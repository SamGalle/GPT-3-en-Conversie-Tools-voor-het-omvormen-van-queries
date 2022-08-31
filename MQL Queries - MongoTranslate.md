In this file you will find MQL queries converted from the SQL queries by the MongoTranslate function from the MongoDB system

### Query 1 
```
db = db.getSiblingDB("admin");
db.getCollection("Tabel1").find({});
```

### Query 2
```
db = db.getSiblingDB("admin");
db.getCollection("Tabel1").find(
    {
        "nummer" : NumberLong(5)
    }
);
```

### Query 3
```
db = db.getSiblingDB("admin");
db.getCollection("Tabel1").find(
    {
        "nummer" : {
            "$lte" : NumberLong(5)
        }
    }
).sort(
    {
        "nummer" : NumberInt(-1)
    }
);
```

### Query 4
```
db = db.getSiblingDB("admin");
db.getCollection("Tabel1").aggregate(
    [
        {
            "$project" : {
                "_id" : NumberInt(0),
                "Tabel1" : "$$ROOT"
            }
        }, 
        {
            "$lookup" : {
                "localField" : "Tabel1.nummer",
                "from" : "Tabel2",
                "foreignField" : "nummer",
                "as" : "Tabel2"
            }
        }, 
        {
            "$unwind" : {
                "path" : "$Tabel2",
                "preserveNullAndEmptyArrays" : true
            }
        }, 
        {
            "$match" : {
                "Tabel1.nummer" : {
                    "$lte" : NumberLong(5)
                }
            }
        }, 
        {
            "$sort" : {
                "Tabel1.nummer" : NumberInt(1)
            }
        }
    ], 
    {
        "allowDiskUse" : true
    }
);
```
### Query 5
```
db = db.getSiblingDB("admin");
db.getCollection("Tabel1").aggregate(
    [
        {
            "$project" : {
                "_id" : NumberInt(0),
                "Tabel1" : "$$ROOT"
            }
        }, 
        {
            "$lookup" : {
                "localField" : "Tabel1.nummer",
                "from" : "Tabel2",
                "foreignField" : "nummer",
                "as" : "Tabel2"
            }
        }, 
        {
            "$unwind" : {
                "path" : "$Tabel2",
                "preserveNullAndEmptyArrays" : true
            }
        }, 
        {
            "$match" : {
                "Tabel1.nummer" : {
                    "$lte" : NumberLong(5)
                }
            }
        }, 
        {
            "$sort" : {
                "Tabel1.nummer" : NumberInt(-1)
            }
        }, 
        {
            "$project" : {
                "Tabel1.naam" : "$Tabel1.naam",
                "Tabel2.kleur" : "$Tabel2.kleur",
                "_id" : NumberInt(0)
            }
        }
    ], 
    {
        "allowDiskUse" : true
    }
);
```
