# Onderzoek model Curie

#### Vraag: Write me a SQL query to get all entries from Tabel1.
Temperatuur optie op 0.72 zetten <br />
Als er achter de vraag geen punt stond, vulde Curie zelf de vraag aan om dan gebaseerd op de vraag een query te schrijven

### SQL Query
```
SELECT * 
FROM Tabel1
```
## Proberen voor een MQL query te genereren
### Poging 1
```
SELECT * 
FROM Tabel1 
This query is translated into the following MongoDB query: SELECT * FROM tab1
```
### Poging 2
```
SELECT "Tabel1"."id" AS "ID","Tabel1"."name" AS "Name","Tabel1"."created_at" AS "CreatedAt","Tabel1"."updated_at" AS "UpdatedAt"} ID Name CreatedAt UpdatedAt
```
### Poging 3
```
SELECT * 
FROM t1
```
### Poging 4
```
SELECT * 
FROM Tabel1 
SELECT * FROM Tabel2
```
### Poging 5
```
SELECT * 
FROM Tabel1 
You can use the following MongoDB command to create a query from text: mongo > db.tables.find('Tabel1')
```
### Poging 6
```
SELECT * 
FROM Tabel1 
Here is a sample output of the above query in MongoDB: [ { "id": 1, "name": "Tabel1", "type": "record", "_id":"1" }, { "id": 2, "name": "_
```
### Poging 7
```
SELECT * 
FROM Tabel1 
This will return all of the data in the table Tabel1.
```
### Poging 8
```
SELECT * 
FROM Tabel1 
This query is equivalent to: SELECT * FROM Tabel1_idx
```
### Poging 9
```
SELECT * 
FROM Tabel1
```
### Poging 10
```
SELECT * 
FROM Tabel1 
This will return all the data in Tabel1.
```
