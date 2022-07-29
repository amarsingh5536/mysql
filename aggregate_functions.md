## Aggregate Functions

* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX`

***REMOVED***

***REMOVED***
+----+----------+---------+----------+--------+---------+
| id | username | country |  salary  | active | age     |
+----+----------+---------+----------+--------+---------+
|  1 | mansih   |   usa   |  20000   |      1 | 24      |
|  2 | amar     |   india |  40000   |      1 | 25      |
|  3 | pallvi   |   india |  40000   |      1 | 25      |
|  4 | mandeep  |   usa   |  50000   |      1 | 28      |
|  5 | sant     |   india |  40000   |      1 | 25      |
|  6 | gaurav   |   canada|  60000   |      1 | 27      |
|  7 | sawan    |   india |  40000   |      1 | 27      |
+----+----------+---------+----------+--------+---------+

***REMOVED***

## Count

***REMOVED*** SELECT COUNT(column_name) FROM table_name; ***REMOVED***

***REMOVED*** select count(salary) as salary_count from employee  where country == 'india'; ***REMOVED***
***REMOVED***
+--------------+
| salary_count |
+--------------+
|            4 |
+--------------+
***REMOVED***

## Average

***REMOVED*** SELECT AVG(column_name) FROM table_name; ***REMOVED***

***REMOVED*** select avg(salary) as avg_salary from employee  where age > 24; ***REMOVED***
***REMOVED***
+------------+
| avg_salary |
+------------+
| 45000.0000 |
+------------+
***REMOVED***

***REMOVED*** select round(avg(salary),2) as avg_salary from employee where age > 24; ***REMOVED***
***REMOVED***
+------------+
| avg_salary |
+------------+
|   45000.00 |
+------------+
***REMOVED***

## Sum

***REMOVED*** SELECT SUM(column_name) FROM table_name; ***REMOVED***

***REMOVED*** select sum(salary) as salay_sum from employee where (age > 24 AND age < 27); ***REMOVED***
***REMOVED***
+-----------+
| salay_sum |
+-----------+
|    120000 |
+-----------+
***REMOVED***

## Min-MAx

***REMOVED***
SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;
***REMOVED***

***REMOVED*** select min(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12"); ***REMOVED***
***REMOVED***
+-----------+
| min_salay |
+-----------+
|     40000 |
+-----------+
***REMOVED***
