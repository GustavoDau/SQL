# SQL
SQL ZOO
# SELECT BASICS
1.
Modify it to show the population of Germany <br />
```
SELECT population FROM world
  WHERE name = 'Germany'
```
2.
Show the name and the population for 'Denmark', 'Finland', 'Norway', 'Sweden'
```
SELECT name, population
FROM world
WHERE name IN ('Norway', 'Sweden', 'Finland','Denmark')
```
