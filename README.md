# SQL
SQL ZOO
# SELECT BASICS

1.Modify it to show the population of Germany. <br />
```
SELECT population FROM world
  WHERE name = 'Germany'
```
2.Show the name and the population for 'Denmark', 'Finland', 'Norway', 'Sweden'.
```
SELECT name, population
FROM world
WHERE name IN ('Norway', 'Sweden', 'Finland','Denmark')
```
3.Show the name and continent where the area is less than 2000 and the gdp is more than 5000000000. <br />
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
3.Show the name and population in millions for the countries of the continent 'South America'. <br />
```
SELECT name, population/1000000 FROM world 
WHERE continent = 'South America'
```
4.Show the name and population for France, Germany, Italy. <br />
```
SELECT name, population FROM world 
WHERE name IN ('France', 'Germany', 'Italy')
```
5.Show the countries which have a name that includes the word 'United'. <br />
```
SELECT name FROM world 
WHERE name LIKE '%united%'
```
6.Show the countries that are big by area or big by population but not both. Show name, population and area. <br />
```
SELECT name, population, area FROM world 
WHERE (area > 3000000 AND population < 250000000) OR (population > 250000000 AND area < 3000000)
```
7.For South America show population in millions and GDP in billions to 2 decimal places. <br />
```
SELECT name, ROUND(population/1000000, 2), ROUND(gdp/1000000000, 2) FROM world 
WHERE continent = 'South America'
```
8.Show the name and capital where the name and the capital have the same number of characters. <br />
```
SELECT name, capital FROM world
WHERE LEN(name)=LEN(capital)
```
9.Show the name and the capital where the first letters of each match. Don't include countries where the name and the capital are the same word. <br />
```
SELECT name FROM world
  WHERE name LIKE '%a%' 
    AND name LIKE '%e%' 
    AND name LIKE '%i%' 
    AND name LIKE '%o%' 
    AND name LIKE '%u%' 
    AND name NOT LIKE '% %'
```
10.Find the country that has all the vowels and no spaces in its name. <br />
```
SELECT name FROM world
  WHERE name LIKE '%a%' 
    AND name LIKE '%e%' 
    AND name LIKE '%i%' 
    AND name LIKE '%o%' 
    AND name LIKE '%u%' 
    AND name NOT LIKE '% %'
```



