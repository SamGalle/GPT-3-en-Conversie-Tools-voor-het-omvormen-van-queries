In this file you will find MQL queries converted from the SQL queries by the GPT-3 model Davinci

### Query 1
```
db.Table1.find();
```

### Query 2
```
db.Tabel1.find({"nummer":5});
```

### Query 3
```
db.Tabel1.find({"nummer":5})
.sort({"nummer":-1});
```

### Query 4
```
db.Tabel1.aggregate([
    {
        $lookup:
        {
            from: "Tabel2",
            localField: "nummer",
            foreignField: "nummer",
            as: "order"
        }
    },
    {
        $match:
        {
            "nummer": {$lte: 5}
        }
    },
    {
        $sort:
        {
            "nummer": 1
        }
    }
])
```

### Query 5 - 2 Pogingen
#### Eerste Poging
```
db.Tabel1.find({
nummer: {$lte: 5}
}).sort({
nummer: -1
}).project({
naam: 1,
"Tabel2 kleur": "$Tabel2.kleur"
})
```
#### Tweede Poging
```

db.Tabel1.aggregate([
    {
        $lookup:
        {
            from: "Tabel2",
            localField: "nummer",
            foreignField: "nummer",
            as: "Tabel1_Tabel2"
        }
    },
    {
        $match:
        {
            "nummer": {$lte: 5}
        }
    },
    {
        $sort:
        {
            "nummer": -1
        }
    },
    {
        $project:
        {
            "Tabel1 naam": "$naam",
            "Tabel2 kleur": "$Tabel1_Tabel2.kleur"
        }
    }
])
```

