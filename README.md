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

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

### 13. Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' OR  CITY  LIKE 'E%' OR CITY  LIKE 'I%' OR CITY  LIKE 'O%' OR CITY  LIKE 'U%');
```

