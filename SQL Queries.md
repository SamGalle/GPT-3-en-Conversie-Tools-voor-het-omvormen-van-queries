### Query 1 

SELECT * FROM Tabel1;

### Query 2
SELECT * FROM Tabel1
WHERE nummer = 5;

### Query 3
SELECT * FROM Tabel1
WHERE nummer <= 5
ORDER BY nummer DESC;

### Query 4
SELECT * FROM Tabel1
Join Tabel2 
ON Tabel1.nummer = Tabel2.nummer
WHERE Tabel1.nummer <= 5
ORDER BY Tabel1.nummer ASC;

### Query 5
SELECT tabel1.naam AS "Tabel1 naam",
tabel2.kleur as "Tabel2 kleur" FROM Tabel1
LEFT JOIN Tabel2 
ON Tabel1.nummer = Tabel2.nummer
WHERE Tabel1.nummer <= 5
ORDER BY Tabel1.nummer DESC;
