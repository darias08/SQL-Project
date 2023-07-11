<h1>Apply Filters to SQL Queries</h1>

<h2>Description</h2>
My company is attempting to strengthen the security of their system. It is my responsibility to make sure the system is secure, look into any potential security vulnerabilities, 
and update employee PCs as needed. The steps that follow demonstrate how I carried out security-related tasks using SQL and filters.
<br />


<h2>Walkthough:</h2>

<h3>Retrieve after hours failed login attempts:</h3>

There was a potential security incident that occurred after business hours (after 18:00). All after
hours login attempts that failed need to be investigated.

<h3></h3>

The following code demonstrates how I created a SQL query to filter for failed login attempts
that occurred after business hours.

![image](https://github.com/darias08/SQL-Project/assets/58616895/d20d5a9b-adf9-4085-9164-f7165e9e7eb1)

The first part of the screenshot is my query, and the second part is a portion of the output. This query filters
for failed login attempts that occurred after `18:00`. First, I started by selecting all data from the `log_in_attempts`
table. Then, I used a `WHERE` clause with an `AND` operator to filter my results to output only login attempts that occurred
after `18:00` and were unsuccessful. The first condition is login_time > `'18:00'`, which filters for the login
attempts that occurred after `18:00`. The second condition is `success = FALSE`, which filters
for the failed login attempts.

<h3>Retrieve login attempts on specific dates: </h3>

A suspicious event occurred on `2022-05-09`. Any login activity that happened on `2022-05-09`
or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that
occurred on specific dates.

![image](https://github.com/darias08/SQL-Project/assets/58616895/723104ad-044d-42a7-bc80-160b0de38806)

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. 
First, I started by selecting all data from the `log_in_attempts` table. Then, I used a WHERE clause with an OR operator to filter my results to output only login 
attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is `login_date = '2022-05-09'`, which filters for logins on 2022-05-09. The second condition is `login_date = '2022-05-08'`, which filters for logins on 2022-05-08.

<h3>Retrieve login attempts outside of Mexico: </h3>
After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.
The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. 

<h3></h3>

![image](https://github.com/darias08/SQL-Project/assets/58616895/7b8845eb-f97b-4b08-b1c4-38f14244a065)


The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. 
First, I started by selecting all data from the `log_in_attempts` table. Then, I used a `WHERE` clause with `NOT` to filter for countries other than Mexico. 
I used `LIKE` with `MEX%` as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign `(%)` represents any number of unspecified characters when used with `LIKE`. 

<h3>Retrieve employees in Marketing</h3>

My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update.
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.

![image](https://github.com/darias08/SQL-Project/assets/58616895/f1a8ebc2-2d76-402c-a521-fd45245e0d16)

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. 
First, I started by selecting all data from the `employees` table. Then, I used a `WHERE` clause with `AND` to filter for `employees` who work in the Marketing department and in the East building. 
I used `LIKE` with `East%` as the pattern to match because the data in the office column represents the East building with the specific office number. 
The first condition is the `department = 'Marketing'` portion, which filters for employees in the Marketing department. The second condition is the office `LIKE 'East%'` portion, 
which filters for employees in the East building.

<h3>Retrieve all employees not in IT: </h3>

My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.
The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.

![image](https://github.com/darias08/SQL-Project/assets/58616895/b3f84567-b2d3-413d-a5a0-441e9f82cb8d)

The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. First, I started by selecting all data from the employees table. Then, I used a `WHERE` clause with `NOT` to filter for `employees` not in this department.


<h2>Summary</h2>

I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, `log_in_attempts` and `employees`. I used the `AND`, `OR`, and `NOT` operators to filter for the specific information needed for each task. I also used `LIKE` and the percentage sign `(%)` wildcard to filter for patterns.

<h2>Languages and Utilities Used</h2>

- <b>Structured Query Language (SQL)</b> 
- <b>Server Version</b> 10.3.39-MariaDB-0+deb10u1 Debian 10

<h2>Environments Used </h2>

- <b>Linux Debian</b>
