
<h2>MYSQL CHEAT SHEET</h2>
<p>All the help you need to kick off your SQL journey</p>

<p>This gist doesn't teach you to download and install MYSQL, so I'm assuming you already have it installed</p>

<h2>MYSQL BASIC ABOUT CREATE USER, PERMISSION, DATABASE, AND TABLE COMMANDS</h2>

<h2>LOGIN FROM TERMINAL</h2>
<div class="highlight highlight-source-shell">
<pre>mysql -u root -p</pre>
</div>

<h2>SHOW USERS</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">SELECT</span> User, Host <span class="pl-k">FROM</span> mysql.user;</pre>
</div>

<h2>CREATE A NEW USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">CREATE USER</span> 'johnDoe'@'localhost' <span class="pl-k">IDENTIFIED BY</span> 'somepassword';</pre>
</div>

<h2>GRANT ALL PRIVELEGES ON ALL DATABASES TO USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">GRANT ALL PRIVILEGES ON * . * TO</span> 'johnDoe'@'localhost';</pre>
</div>
<p>
  Here we granted the user permission to ALL the database functionalities, i.e CREATE, DELETE, INSERT, UPDATE, SELECT     etc. We could also decide what type of permission(s) we wish to grant a user;
</p>


<h2>GRANT ALL PRIVELEGES ON SINGLE DATABASES TO USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">GRANT ALL PRIVILEGES ON blog_data_database.* TO</span> 'johnDoe'@'localhost';</pre>
</div>
<p>
  Here we granted the user(johnDoe) permission to the database(blog_data_database) functionalities, i.e CREATE, DELETE, INSERT, UPDATE, SELECT     etc. We could also decide what type of permission(s) we wish to grant a user;
</p>



<h2>GRANT PRIVELEGE(S) TO USER</h2>
<div class="highlight highlight-source-shell">
  <pre><span class="pl-k">GRANT SELECT, INSERT, DELETE ON *.* TO</span> 'johnDoe'@'localhost';</pre>
</div>
<p>
  Above is a sample syntax where only three privileges are granted to the user.
  <br>
  We then use the "FLUSH PRIVILEGES;" command In order for the changes to take effect and the privileges to be saved.
  <br>
  <hr>
  <strong>NOTE: </strong>All SQL commands must end in a semicolon ;
  <br>
  <hr>
  Here is a list of the MySQL privileges which are most commonly used:
  <ul>
    <li>ALL PRIVILEGES – grants all privileges to the MySQL user</li>
    <li>CREATE – allows the user to create databases and tables</li>
    <li>DROP - allows the user to drop databases and tables</li>
    <li>DELETE - allows the user to delete rows from specific MySQL table</li>
    <li>INSERT - allows the user to insert rows into specific MySQL table</li>
    <li>SELECT – allows the user to read the database</li>
    <li>UPDATE - allows the user to update table rows</li>
  </ul>
</p>

<h2>IN ORDER FOR THE CHANGES TO TAKE EFFECT</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">FLUSH PRIVILEGES;</span></pre>
</div>

<h2>SHOW GRANTS GIVEN TO A USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-sk">SHOW GRANTS FOR</span> 'johnDoe'@'localhost';</pre>
</div>

<h2>REMOVE GRANTS GIVEN TO USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">REVOKE ALL PRIVILEGES, GRANT OPTION FROM</span> 'someuser'@'localhost';</pre>
</div>

<h2>DELETE USER</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">DROP USER</span> 'johnDoe'@'localhost';</pre>
</div>

<h2>EXIT</h2>
<div class="highlight highlight-source-shell">
<pre>Exit;</pre>
</div>

<h2>LOGIN AS USER YOU CREATED</h2>
<div class="highlight highlight-source-shell">
<pre>mysql -u johnDoe -p</pre>
</div>

<h2>SHOW ALL DATABASE YOUR USER HAS</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">SHOW DATABASES;</span></pre>
</div>

<h2>CREATE A DATABASE</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">CREATE DATABASE</span> sql_class;</pre>
</div>

<h2>DELETE A DATABASE</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">DROP DATABASE</span> sql_class;</pre>
</div>

<h2>SELECT A DATABASE</h2>
<div class="highlight highlight-source-shell">
<pre><span class="pl-k">USE</span> sql_class;</pre>
</div>

<h2>CREATE TABLE</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">CREATE TABLE</span> users(
id <span class="pl-s">INT AUTO_INCREMENT</span>,
first_name <span class="pl-s">VARCHAR(100)</span>,
last_name <span class="pl-s">VARCHAR(100)</span>,
email <span class="pl-s">VARCHAR(50)</span>,
password <span class="pl-s">VARCHAR(20)</span>,
location <span class="pl-s">VARCHAR(100)</span>,
dept <span class="pl-s">VARCHAR(100)</span>,
is_admin <span class="pl-s">TINYINT(1)</span>,
register_date <span class="pl-s">DATETIME</span>,
<span class="pl-s">PRIMARY KEY(id)</span>
);
</pre>
</div>

<h2>DELETE TABLE</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">DROP TABLE</span> table_name;
</pre>
</div>

<h2>SHOW TABLES</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">SHOW TABLES</span>;
</pre>
</div>

<h2>INSERT ROW/RECORDS</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">INSERT INTO</span> users (first_name, last_name, email, password, location, dept, is_admin, register_date) <span class="pl-k">VALUES</span> (<span class="pl-s">'Justice', 'Eziefule', 'justice@gmail.com', '123456','Florida', 'development', 1, now()</span>);
</pre>
</div>

<h2>INSERT MULTIPLE ROW/RECORDS</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">INSERT INTO</span> users (first_name, last_name, email, password, location, dept, is_admin, register_date) <span class="pl-k">VALUES</span> (<span class="pl-s">'Fred', 'Smith', 'fred@gmail.com', '123456', 'New York', 'design', 0, now()</span>), (<span class="pl-s">'Sara', 'Watson', 'sara@gmail.com', '123456', 'New York', 'design', 0, now()</span>),(<span class="pl-s">'Will', 'Jackson', 'will@yahoo.com', '123456', 'London', 'development', 1, now()</span>),(<span class="pl-s">'Paula', 'Johnson', 'paula@yahoo.com', '123456', 'Massachusetts', 'sales', 0, now()</span>),(<span class="pl-s">'Tom', 'Spears', 'tom@yahoo.com', '123456', 'Manchester', 'sales', 0, now()</span>);
</pre>
</div>

<h2>SELECT ALL DATA FROM TABLE</h2>
<div class="highlight highlight-source-shell">
<pre>
<span class="pl-k">SELECT * FROM</span> users;
</pre>
<p><strong>*</strong> is a syntax that represents <strong>ALL</strong>
</div>

<h2>SELECT SPECIFIC DATA FROM TABLE</h2>
<div class="highlight highlight-source-shell">
<pre>
   SELECT first_name, last_name FROM users;
</pre>
<p>
 <pre>
  SELECT location FROM users;
</pre>
</p>
</div>

<h2>WHERE CLAUSE</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT * FROM users WHERE location='Massachusetts';
SELECT * FROM users WHERE location='Massachusetts' AND dept='sales';
SELECT * FROM users WHERE is_admin = 1;
SELECT * FROM users WHERE is_admin > 0;
</pre>
</div>

<h2>DELETE ROW</h2>
<div class="highlight highlight-source-shell">
<pre>
   DELETE FROM users WHERE id = 6;
</pre>
</div>


<h2>UPDATE ROW</h2>
<div class="highlight highlight-source-shell">
<pre>
   UPDATE users SET email = 'freddy@gmail.com' WHERE id = 2;
</pre>
</div>

<h2>ADD NEW COLUMN</h2>
<div class="highlight highlight-source-shell">
<pre>
 ALTER TABLE users ADD date_of_birth DATETIME;
</pre>
</div>

<h2>MODIFY COLUMN</h2>
<div class="highlight highlight-source-shell">
<pre>
 ALTER TABLE users MODIFY COLUMN date_of_birth DATE;
</pre>
</div>

<h2>DELETE ROW</h2>
<div class="highlight highlight-source-shell">
<pre>
DELETE FROM users WHERE id = 6;
</pre>
</div>

<h2>CONCATENATE COLUMNS</h2>
<p>With concatenate comes the AS syntax</p>
<div class="highlight highlight-source-shell">
<pre>
SELECT CONCAT(first_name, ' ', last_name) AS 'Name', dept FROM users;
</pre>
</div>

<h2>SELECT DISTINCT LOCATION</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT DISTINCT location FROM users;
</pre>
</div>

<h2>BETWEEN (SELECT RANGE)</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT * FROM users WHERE age BETWEEN 20 AND 25;
</pre>
</div>

<h2>LIKE (SEARCHING)</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT * FROM users WHERE dept LIKE 'd%';
SELECT * FROM users WHERE dept LIKE 'dev%';
SELECT * FROM users WHERE dept LIKE '%t';
SELECT * FROM users WHERE dept LIKE '%e%';
</pre>
</div>

<h2>NOT LIKE (SEARCHING)</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT * FROM users WHERE dept NOT LIKE 'd%';
</pre>
</div>

<h2>IN</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT * FROM users WHERE dept IN ('design', 'sales');
</pre>
</div>

<h2>CREATE TABLE FOR posts</h2>
<div class="highlight highlight-source-shell">
<pre>
CREATE TABLE posts(
id INT AUTO_INCREMENT,
   user_id INT,
   title VARCHAR(100),
   body TEXT,
   publish_date DATETIME DEFAULT CURRENT_TIMESTAMP,
   PRIMARY KEY(id),
   FOREIGN KEY (user_id) REFERENCES users(id)
);
</pre>
</div>

<h2>ADD DATA TO posts</h2>
<div class="highlight highlight-source-shell">
<pre>
INSERT INTO posts(user_id, title, body) VALUES (1, 'Post One', 'This is post one'),(3, 'Post Two', 'This is post two'),(1, 'Post Three', 'This is post three'),(2, 'Post Four', 'This is post four'),(5, 'Post Five', 'This is post five'),(4, 'Post Six', 'This is post six'),(2, 'Post Seven', 'This is post seven'),(1, 'Post Eight', 'This is post eight'),(3, 'Post Nine', 'This is post none'),(4, 'Post Ten', 'This is post ten');
</pre>
</div>

<h2>ADD DATA TO posts</h2>
<div class="highlight highlight-source-shell">
<pre>
INSERT INTO posts(user_id, title, body) VALUES (1, 'Post One', 'This is post one'),(3, 'Post Two', 'This is post two'),(1, 'Post Three', 'This is post three'),(2, 'Post Four', 'This is post four'),(5, 'Post Five', 'This is post five'),(4, 'Post Six', 'This is post six'),(2, 'Post Seven', 'This is post seven'),(1, 'Post Eight', 'This is post eight'),(3, 'Post Nine', 'This is post none'),(4, 'Post Ten', 'This is post ten');
</pre>
</div>

<h2>INNER JOIN</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT
  users.first_name,
  users.last_name,
  posts.title,
  posts.publish_date
FROM users
INNER JOIN posts
ON users.id = posts.user_id
ORDER BY posts.title;
</pre>
</div>

<h2>INNER JOIN</h2>
<div class="highlight highlight-source-shell">
<pre>
CREATE TABLE comments(
	id INT AUTO_INCREMENT,
  post_id INT,
  user_id INT,
  body TEXT,
  publish_date DATETIME DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY(id),
  FOREIGN KEY(user_id) references users(id),
  FOREIGN KEY(post_id) references posts(id)
);
</pre>
</div>

<h2>ADD DATA TO comments TABLE</h2>
<div class="highlight highlight-source-shell">
<pre>
INSERT INTO comments(post_id, user_id, body) VALUES (1, 3, 'This is comment one'),(2, 1, 'This is comment two'),(5, 3, 'This is comment three'),(2, 4, 'This is comment four'),(1, 2, 'This is comment five'),(3, 1, 'This is comment six'),(3, 2, 'This is comment six'),(5, 4, 'This is comment seven'),(2, 3, 'This is comment seven');
</pre>
</div>

<h2>LEFT JOIN</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT
comments.body,
posts.title
FROM comments
LEFT JOIN posts ON posts.id = comments.post_id
ORDER BY posts.title;
</pre>
</div>

<h2>JOIN MULTIPLE TABLES</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT
comments.body,
posts.title,
users.first_name,
users.last_name
FROM comments
INNER JOIN posts on posts.id = comments.post_id
INNER JOIN users on users.id = comments.user_id
ORDER BY posts.title;
</pre>
</div>

<h2>JOIN MULTIPLE TABLES</h2>
<div class="highlight highlight-source-shell">
<pre>
SELECT
comments.body,
posts.title,
users.first_name,
users.last_name
FROM comments
INNER JOIN posts on posts.id = comments.post_id
INNER JOIN users on users.id = comments.user_id
ORDER BY posts.title;
</pre>
</div>

<hr>

# RELATIONSHIPS IN A RELATIONAL DATABASE

There are 3 types of relationships in database designs

1. One-to-One

2. One-to-Many (or Many-to-One)

3. Many-to-Many


## ONE-to-ONE (1:1)

<img src="https://database.guide/wp-content/uploads/2016/05/relationship-diagram-one-to-one.png" alt="Image example of a 1:1 relationship" />

This is not a common relationship type, as the data stored in table pay could just have easily been stored in table Employee. However, there are some valid reasons for using this relationship type. A one-to-one relationship  can be used for security purposes, to divide a large table, and various other specific purposes.

In the above example, we could just as easily have put an HourlyRate field straight into the Employee table and not bothered with the Pay table. However, hourly rate could be sensitive data that only certain database users should see. So, by putting the hourly rate into a separate table, we can provide extra security around the Pay table so that only certain users can access the data in that table.


## ONE-to-MANY (1:n)

This is the most common relationship type. In this type of relationship, a row in table A can have many matching rows in table B, but a row in table B can have only one matching row in table A.

<img src="https://database.guide/wp-content/uploads/2016/05/relationship-diagram-one-to-many.png" alt="Image example of 1:n relationship" />

One-to-Many relationships can also be viewed as Many-to-One relationships, depending on which way you look at it.

In the above example, the Customer table is the “many” and the City table is the “one”. Each customer can only be assigned one city,. One city can be assigned to many customers.


## MANY-to-MANY (n:m)

In a many-to-many relationship, a row in table A can have many matching rows in table B, and vice versa.

A many-to-many relationship could be thought of as two one-to-many relationships, linked by an intermediary table.

The intermediary table is typically referred to as a “junction table” (also as a “cross-reference table”). This table is used to link the other two tables together. It does this by having two fields that reference the primary key of each of the other two tables.

The following is an example of a many-to-many relationship:

<img src="https://database.guide/wp-content/uploads/2016/05/create_a_relationship_in_access_2013_5.png" alt="Image example of a n:m relationship" />

So in order to create a many-to-many relationship between the Customers table and the Products table, we created a new table called Orders.

In the Orders table, we have a field called CustomerId and another called ProductId. The values that these fields contain should correspond with a value in the corresponding field in the referenced table. So any given value in Orders.CustomerId should also exist in the Customer.CustomerId field.
