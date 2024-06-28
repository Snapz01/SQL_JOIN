# SQL Join exercise
#
#
# 1: Get the cities with a name starting with ping sorted by their population with the least populated cities first
#SELECT Name, Population FROM world.city ORDER BY Population ASC;
#
# 2: Get the cities with a name starting with ran sorted by their population with the most populated cities first
#SELECT Name, Population FROM world.city ORDER BY  Population DESC;
#
# 3: Count all cities
#SELECT COUNT(name) AS 'Number of cities' FROM world.city;
#
# 4: Get the average population of all cities
#SELECT AVG(Population) AS 'Avrage Population' FROM world.city;
#
# 5: Get the biggest population found in any of the cities
#SELECT name, Population FROM world.city ORDER BY Population DESC limit 1;
#
# 6: Get the smallest population found in any of the cities
#SELECT name, Population FROM world.city ORDER BY Population ASC limit 1;
#
# 7: Sum the population of all cities with a population below 10000
#SELECT sum(Population) as 'Sum of Population' FROM world.city WHERE Population < 10000;
#
# 8: Count the cities with the countrycodes MOZ and VNM
#SELECT count(ID) AS 'Cites with Contrycode \n"MOZ and "VNM"' FROM world.city WHERE CountryCode IN ('MOZ', 'VNM');
#
# 9: Get individual count of cities for the countrycodes MOZ and VNM
#SELECT CountryCode, COUNT(Name) AS 'Number of Cities' FROM world.city WHERE CountryCode IN ('MOZ', 'VNM') GROUP BY CountryCode;
#
# 10: Get average population of cities in MOZ and VNM
#SELECT AVG(Population) AS 'Average Population in \nMOZ and VNM' FROM world.city WHERE CountryCode IN ('MOZ', 'VNM');
#
# 11: Get the countrycodes with more than 200 cities
#SELECT CountryCode, COUNT(Name) AS 'Number of Cities' FROM world.city GROUP BY CountryCode HAVING COUNT(Name) > 200;
#
# 12: Get the countrycodes with more than 200 cities ordered by city count
#SELECT CountryCode, COUNT(Name) AS 'Number of Cities' FROM world.city GROUP BY CountryCode HAVING COUNT(Name) > 200 ORDER BY COUNT(Name) DESC;
#
# 13: What language(s) is spoken in the city with a population between 400 and 500 ?
#SELECT Language, Population FROM world.city JOIN world.countrylanguage WHERE Population BETWEEN 400 AND 500;
#
# 14: What are the name(s) of the cities with a population between 500 and 600 people and the language(s) spoken in them
#SELECT Language, Name, Population FROM world.city JOIN world.countrylanguage WHERE Population BETWEEN 500 AND 600;
#
# 15: What names of the cities are in the same country as the city with a population of 122199 (including the that city itself)
#SELECT c.Name AS CityName, co.Name AS CountryName FROM world.city c
#JOIN world.country co ON c.CountryCode = co.Code WHERE c.CountryCode = (
#SELECT CountryCode FROM world.city WHERE Population = 122199);
#
# 16: What names of the cities are in the same country as the city with a population of 122199 (excluding the that city itself)
#
#
# 17: What are the city names in the country where Luanda is capital?
#
#
# 18: What are the names of the capital cities in countries in the same region as the city named Yaren
#
#
# 19: What unique languages are spoken in the countries in the same region as the city named Riga
#
#
# 20: Get the name of the most populous city
#SELECT Name, Population FROM world.city ORDER BY Population DESC LIMIT 1;
