## Aggregate Functions

* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX`

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

***REMOVED*** select min(salary), username from employee where (date > "2022-01-01" AND date < "2022-31-12"); ***REMOVED***
***REMOVED***
+-----------+
| min_salay |
+-----------+
|     20000 |
+-----------+
***REMOVED***
