## Aggregate Functions

* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX`

## Count

***REMOVED*** SELECT COUNT(column_name) FROM table_name; ***REMOVED***

* example: ***REMOVED*** select count(salary) as salary_count from employee  where salary > "40000"; ***REMOVED***


## Average

***REMOVED*** SELECT AVG(column_name) FROM table_name; ***REMOVED***

* example: ***REMOVED*** select avg(salary) from employee  where date > "1994-10-01"; ***REMOVED***

* example 2: ***REMOVED*** select round(avg(salary),2) from employee where date > "1994-10-01"; ***REMOVED***


## Sum

***REMOVED*** SELECT SUM(column_name) FROM table_name; ***REMOVED***

* example: ***REMOVED*** select sum(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12"); ***REMOVED***


## Min-MAx

***REMOVED***
SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;
***REMOVED***

* example: ***REMOVED*** select min(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12"); ***REMOVED***

* example: ***REMOVED*** select max(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12"); ***REMOVED***




