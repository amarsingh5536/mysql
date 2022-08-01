The GROUP BY statement is used with aggregate functions  like:
* `AVG`
* `SUM`
* `COUNT`
* `MIN`
* `MAX` 

to group the result-set by one or more columns.

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
## GROUP BY WITH COUNT

```
SELECT country, COUNT(*) AS emp_count FROM employee GROUP BY country;
```

```
+---------+-----------+
| country | emp_count |
+---------+-----------+
| canada  |         1 |
| india   |         4 |
| usa     |         2 |
+---------+-----------+

```
## GROUP BY WITH SUM

```
 SELECT country, SUM(salary) AS total_salary FROM  employee group by country;
```

```
+---------+--------------+
| country | total_salary |
+---------+--------------+
| canada  |        60000 |
| india   |       160000 |
| usa     |        70000 |
+---------+--------------+

```

## GROUP BY WITH SUM AND HAVING CLAUSE
* We use `HAVING` insted of `WHERE` to filter out the condition in group by. 

```
SELECT country, SUM(salary) AS total_salary FROM  employee group by country HAVING total_salary > 60000;
```
```

+---------+--------------+
| country | total_salary |
+---------+--------------+
| india   |       160000 |
| usa     |        70000 |
+---------+--------------+

```

## GROUP BY WITH AVG

```
SELECT country, age , AVG(age) as avg_salary FROM employee GROUP BY country, age;
```

```
+---------+------+------------+
| country | age  | avg_salary |
+---------+------+------------+
| canada  |   27 |    27.0000 |
| india   |   25 |    25.0000 |
| india   |   27 |    27.0000 |
| usa     |   24 |    24.0000 |
| usa     |   28 |    28.0000 |
+---------+------+------------+

```

## GROUP BY WITH MAX

```
SELECT age , MAX(salary) as max_salary FROM employee GROUP BY age;
```
```
+------+------------+
| age  | max_salary |
+------+------------+
|   24 |      20000 |
|   25 |      40000 |
|   27 |      60000 |
|   28 |      50000 |
+------+------------+
```


