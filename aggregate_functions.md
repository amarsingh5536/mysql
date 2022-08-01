## Aggregate Functions

* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX`

## TABLE EMPLOYEE

```
+----+----------+---------+------+--------+--------+------------+
| id | username | country | age  | salary | active | date       |
+----+----------+---------+------+--------+--------+------------+
|  1 | manish   | usa     |   24 |  20000 |      1 | 2022-07-29 |
|  2 | amar     | india   |   25 |  40000 |      1 | 2022-07-29 |
|  3 | pallvi   | india   |   25 |  40000 |      1 | 2022-07-29 |
|  4 | mandeep  | usa     |   28 |  50000 |      1 | 2022-07-29 |
|  5 | sant     | india   |   25 |  40000 |      1 | 2022-07-29 |
|  6 | gaurav   | canada  |   27 |  60000 |      1 | 2022-07-29 |
|  7 | sawan    | india   |   27 |  40000 |      1 | 2022-07-29 |
+----+----------+---------+------+--------+--------+------------+

```

## Count

``` SELECT COUNT(column_name) FROM table_name; ```

``` select count(salary) as salary_count from employee  where country == 'india'; ```
```
+--------------+
| salary_count |
+--------------+
|            4 |
+--------------+
```

## Average

``` SELECT AVG(column_name) FROM table_name; ```

``` select avg(salary) as avg_salary from employee  where age > 24; ```
```
+------------+
| avg_salary |
+------------+
| 45000.0000 |
+------------+
```

``` select round(avg(salary),2) as avg_salary from employee where age > 24; ```
```
+------------+
| avg_salary |
+------------+
|   45000.00 |
+------------+
```

## Sum

``` SELECT SUM(column_name) FROM table_name; ```

``` select sum(salary) as salay_sum from employee where (age > 24 AND age < 27); ```
```
+-----------+
| salay_sum |
+-----------+
|    120000 |
+-----------+
```

## Min-MAx

```
SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;
```

``` select min(salary), username from employee where (date > "2022-01-01" AND date < "2022-31-12"); ```
```
+-----------+
| min_salay |
+-----------+
|     20000 |
+-----------+
```
