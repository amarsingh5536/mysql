## TABLE EMPLOYEE


+----+----------+---------+------+--------+--------+------------+
| id | username | country | age  | salary | active | date       |
+----+----------+---------+------+--------+--------+------------+
|  1 | manish   | usa     |   24 |  20000 |      1 | 2022-07-29 |
|  2 | amar     | india   |   25 |  40000 |      1 | 2022-07-29 |
|  3 | pallvi   | india   |   25 |  40000 |      1 | 2022-07-29 |
|  4 | mandeep  | usa     |   28 |  50000 |      1 | 2022-07-29 |
|  5 | sant     | india   |   25 |  40000 |      1 | 2022-07-29 |
|  6 | gaurav   | canada  |   27 |  60000 |      0 | 2022-07-29 |
|  7 | sawan    | india   |   27 |  40000 |      1 | 2022-07-29 |
+----+----------+---------+------+--------+--------+------------+

## Example 1:


SELECT username, active, 
CASE 
  WHEN active = 1 THEN "true"     
  WHEN active = 0 THEN "fasle"    
  ELSE "fasle" 
END as is_acitve FROM employee;


+----------+--------+-----------+
| username | active | is_acitve |
+----------+--------+-----------+
| manish   |      1 | true      |
| amar     |      1 | true      |
| pallvi   |      1 | true      |
| mandeep  |      1 | true      |
| sant     |      1 | true      |
| gaurav   |      0 | false     |
| sawan    |      1 | true      |
+----------+--------+-----------+
