# Feladat megoldás

> Első feladat
```sql
SELECT orszag FROM orszagok WHERE orszag != 'MAGYARORSZÁG' ORDER BY ABS(terulet - (SELECT terulet FROM orszagok WHERE orszag = 'MAGYARORSZÁG')) ASC LIMIT 1;
```

> Második feladat
```sql
SELECT (SELECT SUM(nepesseg) FROM orszagok WHERE foldr_hely LIKE '%Ázsia%') / SUM(nepesseg) * 100 FROM orszagok;
```

> Harmadik feladat
```sql
SELECT orszag FROM orszagok WHERE gdp / 2 = (SELECT AVG(gdp) FROM orszagok);
```

> Negyedik feladat
```sql
SELECT COUNT(DISTINCT penznem) FROM orszagok WHERE foldr_hely LIKE '%Európa%' AND penznem NOT LIKE 'euró';
```

> Ötödik feladat
```sql
SELECT penznem FROM orszagok GROUP BY penznem HAVING COUNT(*) > 1;
```

> Hatodik feladat
```sql
SELECT orszag FROM orszagok GROUP BY allamforma HAVING COUNT(*) = 1;
```