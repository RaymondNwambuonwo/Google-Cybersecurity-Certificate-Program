# Complete a SQL JOIN

## In this lab activity, you’ll use SQL joins to connect separate tables and retrieve needed information

### Scenario

In this scenario, you’ll investigate a recent security incident that compromised some machines. You are responsible for getting the required information from the database for the investigation. Here’s how you’ll do this task: First, you’ll use an inner join to identify which employees are using which machines. Second, you’ll use left and right joins to find machines that do not belong to any specific user and users who do not have any specific machine assigned to them. Finally, you’ll use an inner join to list all login attempts made by all employees.

```SQL
SELECT *
FROM machines;

SELECT *
FROM machines
INNER JOIN employees ON machines.device_id = employees.device_id;

SELECT *
FROM machines
LEFT JOIN employees ON machines.device_id = employees.device_id;

SELECT *
FROM machines
RIGHT JOIN employees ON machines.device_id = employees.device_id;

SELECT *
FROM employees
INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;
```
