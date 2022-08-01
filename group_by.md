The GROUP BY statement is used with aggregate functions  like:
* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX` 

to group the result-set by one or more columns.

***REMOVED***

***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
***REMOVED***
|  6 | gaurav   | canada  |   27 |  60000 |      1 | 2022-07-29 |
***REMOVED***
***REMOVED***

***REMOVED***
## GROUP BY WITH COUNT

***REMOVED***
SELECT country, COUNT(*) AS emp_count FROM employee GROUP BY country;
***REMOVED***

***REMOVED***
+---------+-----------+
| country | emp_count |
+---------+-----------+
| canada  |         1 |
| india   |         4 |
| usa     |         2 |
+---------+-----------+

***REMOVED***
## GROUP BY WITH SUM

***REMOVED***
 SELECT country, SUM(salary) AS total_salary FROM  employee group by country;
***REMOVED***

***REMOVED***
+---------+--------------+
| country | total_salary |
+---------+--------------+
| canada  |        60000 |
| india   |       160000 |
| usa     |        70000 |
+---------+--------------+

***REMOVED***

## GROUP BY WITH SUM AND HAVING CLAUSE
* WE use `HAVING` insted of `WHERE` to filter out the condition. 

***REMOVED***
SELECT country, SUM(salary) AS total_salary FROM  employee group by country HAVING total_salary > 60000;
***REMOVED***
***REMOVED***

+---------+--------------+
| country | total_salary |
+---------+--------------+
| india   |       160000 |
| usa     |        70000 |
+---------+--------------+

***REMOVED***

## GROUP BY WITH AVG

***REMOVED***
SELECT country, age , AVG(age) as avg_salary FROM employee GROUP BY country, age;
***REMOVED***

***REMOVED***
+---------+------+------------+
| country | age  | avg_salary |
+---------+------+------------+
| canada  |   27 |    27.0000 |
| india   |   25 |    25.0000 |
| india   |   27 |    27.0000 |
| usa     |   24 |    24.0000 |
| usa     |   28 |    28.0000 |
+---------+------+------------+

***REMOVED***

## GROUP BY WITH MAX

***REMOVED***
SELECT age , MAX(salary) as max_salary FROM employee GROUP BY age;
***REMOVED***
***REMOVED***
+------+------------+
| age  | max_salary |
+------+------------+
|   24 |      20000 |
|   25 |      40000 |
|   27 |      60000 |
|   28 |      50000 |
+------+------------+
***REMOVED***


