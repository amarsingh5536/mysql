## Aggregate Functions

* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX`

## Count
SELECT COUNT(column_name) FROM table_name;

* example: select count(salary) as salary_count from employee  where salary > "40000";


## Average
SELECT AVG(column_name) FROM table_name;

select avg(salary) from employee  where date > "1994-10-01";

* example: select avg(salary) from employee  where date > "1994-10-01";

* example 2: select round(avg(salary),2) from employee where date > "1994-10-01";


## Sum

SELECT SUM(column_name) FROM table_name;

* example: select sum(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12");


## Min-MAx

SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;

* example: select min(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12");

* example: select max(salary) from employee where (date > "1994-01-01" AND date < "1994-31-12");




