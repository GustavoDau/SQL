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
9.Find the country that has all the vowels and no spaces in its name. <br />
```
SELECT name FROM world
  WHERE name LIKE '%a%' 
    AND name LIKE '%e%' 
    AND name LIKE '%i%' 
    AND name LIKE '%o%' 
    AND name LIKE '%u%' 
    AND name NOT LIKE '% %'
```
10.Show the name and capital where the name and the capital have the same number of characters. <br />
```
SELECT name, capital FROM world
  WHERE LEN(name)=LEN(capital)
```
11.Show the name and the capital where the first letters of each match. Don't include countries where the name and the capital are the same word. <br />
```
SELECT name, capital
  FROM world
  WHERE LEFT(name, 1) = LEFT(capital, 1) AND name <> capital
```
# SELECT from Nobel
1. Show who won the 1962 prize for literature. <br />
```
SELECT winner FROM nobel
WHERE yr = 1962 AND subject = 'Literature'
```
2.Show the year and subject that won 'Albert Einstein' his prize. <br />
```
SELECT yr, subject FROM nobel
WHERE winner = 'Albert Einstein'
```
3.Give the name of the 'peace' winners since the year 2000, including 2000. <br />
```
SELECT winner FROM nobel
 WHERE yr >= 2000 AND subject = 'Peace'
```
4.Show all details (yr, subject, winner) of the literature prize winners for 1980 to 1989 inclusive. <br />
```
SELECT yr, subject, winner FROM nobel
WHERE yr >= 1980 AND yr <= 1989 AND subject = 'Literature'
```
5.Show all details of the presidential winners <br />
```
SELECT * FROM nobel
WHERE winner IN ('Theodore Roosevelt', 'Woodrow Wilson','Jimmy Carter', 'Barack Obama')
```
6.Show the year, subject, and name of physics winners for 1980 together with the chemistry winners for 1984. <br />
```
SELECT * FROM nobel
WHERE (subject = 'Physics' AND yr = 1980) OR (subject = 'Chemistry' AND yr = 1984)
```
7.Show the year, subject, and name of winners for 1980 excluding chemistry and medicine. <br />
```
SELECT * FROM nobel
WHERE yr = 1980 AND subject NOT IN ('Chemistry', 'Medicine')
```
8.
