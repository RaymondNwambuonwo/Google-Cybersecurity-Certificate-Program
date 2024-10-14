# Filter SQL queries

## In this lab activity, I’ll apply basic filters to SQL queries to retrieve information from a MariaDB database

### Scenario

In this scenario, you need to get specific information about employees, their machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine. You are responsible for finding the required information by querying a database. You’ll add filters to your queries to locate the information more quickly. Here’s how you’ll do this task: First, you’ll list all organization machines and their operating systems. Second, you’ll list all machines with the operating system OS 2. Third, you’ll list all the employees in the Finance and Sales departments. Fourth, you’ll obtain information about machines.

```SQL
SELECT device_id, operating_system
FROM machines;

SELECT device_id, operating_system
FROM machines
WHERE operating_system = 'OS 2';

SELECT *
FROM employees
WHERE department = 'Finance';

SELECT *
FROM employees
WHERE department = 'Sales';

SELECT *
FROM employees
WHERE office = 'South-109';

SELECT *
FROM employees
WHERE office LIKE 'South%';
```
