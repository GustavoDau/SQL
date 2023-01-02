# SQL
SQL ZOO
# SELECT BASICS

1.Modify it to show the population of Germany <br />
```
SELECT population FROM world
  WHERE name = 'Germany'
```
2.Show the name and the population for 'Denmark', 'Finland', 'Norway', 'Sweden'
```
SELECT name, population
FROM world
WHERE name IN ('Norway', 'Sweden', 'Finland','Denmark')
```
3.Show the name and continent where the area is less than 2000 and the gdp is more than 5000000000 <br />
```
SELECT name , continent
FROM world
WHERE area < 2000
AND gdp > 5000000000
```
# SELECT from WORLD

1.Read the notes about this table. Observe the result of running this SQL command to show the name, continent and population of all countries. <br />
```
SELECT name FROM world
WHERE population>=200000000
```
2.Give the name and the per capita GDP for those countries with a population of at least 200 million. <br />
```
SELECT name, gdp/population FROM world 
WHERE population>200000000
```
3.Show the name and population in millions for the countries of the continent 'South America' <br />
```
SELECT name, population/1000000 FROM world 
WHERE continent = 'South America'
```
4.Show the name and population for France, Germany, Italy <br />
```
SELECT name, population FROM world 
WHERE name IN ('France', 'Germany', 'Italy')
```


