# Easy.  

### 8. Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.  


```
SELECT DISTINCT CITY FROM STATION WHERE RIGHT(CITY,1) IN ('a','e','i','o','u');
```
### 9. Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.


```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(CITY,1) IN ('a','e','i','o','u')
```

### 10. Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.


```
SELECT CITY, LENGTH(CITY) FROM STATION
ORDER BY LENGTH(CITY),CITY ASC
LIMIT 1;
SELECT CITY, LENGTH(CITY) FROM STATION
ORDER by LENGTH(CITY) DESC
LIMIT 1;
```

### 11. Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.


```
SELECT (COUNT(CITY) - COUNT(DISTINCT CITY)) FROM STATION;
```

### 12. Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY FROM STATION 
WHERE LEFT(CITY,1) IN ('a','e','i','o','u') 
AND RIGHT(CITY, 1) IN ('a','e','i','o','u')
```
### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 14. Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
OR RIGHT(CITY, 1) NOT IN ('a', 'e', 'i', 'o', 'u');
```

### 15. Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY FROM STATION WHERE RIGHT(CITY, 1) NOT IN ('a', 'e', 'i', 'o', 'u');
```

### 16. Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
OR RIGHT(CITY, 1) NOT IN ('a', 'e', 'i', 'o', 'u');
```

### 17. Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY FROM STATION WHERE (LEFT(CITY,1) NOT IN ('a','e','i','o','u')
AND RIGHT(CITY,1) NOT IN ('a','e','i','o','u'));
```

### 18. Query the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

```
SELECT NAME FROM STUDENTS WHERE MARKS > 75 ORDER BY RIGHT(NAME, 3), ID ASC;
```

### 19. Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.

```
SELECT name FROM Employee ORDER BY name;
```

### 20. Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than  per month who have been employees for less than 10 months. Sort your result by ascending employee_id.

```
SELECT name FROM Employee
WHERE salary > 2000 AND months < 10
ORDER BY employee_id;
```
### 21. Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:



```
SELECT CASE             
            WHEN A + B > C AND B + C > A AND A + C > B THEN
                CASE 
                    WHEN A = B AND B = C THEN 'Equilateral'
                    WHEN A = B OR B = C OR A = C THEN 'Isosceles'
                    ELSE 'Scalene'
                END
            ELSE 'Not A Triangle'
        END
FROM TRIANGLES;
```
### 22. Query a count of the number of cities in CITY having a Population larger than 100000 .



```
SELECT COUNT(NAME)
FROM CITY
WHERE POPULATION > 100000
```

