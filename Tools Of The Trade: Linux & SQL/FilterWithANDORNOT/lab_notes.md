# Filter with `AND`, `OR`, and `NOT`

## In this lab activity, I’ll use the `AND`, `OR`, and `NOT` operators to create more complex filters for SQL queries

### Scenario

In this scenario, you need to obtain specific information about employees, their machines, and the departments they belong to from the database. Your team needs data to investigate potential security issues and to update computers. You are responsible for filtering the required information from the database. Here’s how you’ll do this task: First, you’ll retrieve all failed login attempts after business hours. Second, you’ll retrieve all login attempts that occurred on specific dates. Third, you’ll retrieve logins that didn't originate in Mexico. Fourth, you’ll retrieve information about certain employees in the Marketing department. Fifth, you’ll retrieve information about employees in the Finance or the Sales department. Finally, you’ll obtain information about employees who are not in the Information Technology department.

> **Note:** Values of `TRUE` and `FALSE` are not placed in single quotes because they are not string data. They are Boolean data, which is another data type.

```SQL
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;

SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';

SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';

SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';

SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';

SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```
