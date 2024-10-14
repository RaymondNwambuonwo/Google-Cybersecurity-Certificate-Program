# Perform a SQL Query

## In this lab activity, I use `SELECT` and `FROM` in SQL to return the information I need from a database. You’ll also use the `ORDER BY` keyword to sequence the information returned by a query based on a specified column

### Scenario

In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.The information you need is located in the machines and login_attempts tables in the organization database. Here’s how you’ll do this task: First, you’ll obtain information on the employee devices that must be updated. Next, you’ll examine the login attempts for unusual activity. Finally, you’ll use the `ORDER BY` keyword to sort the data returned by your SQL queries.

```bash
sudo mysql organization
```

```SQL
SELECT *
FROM machines;

SELECT device_id, email_client
FROM machines;

SELECT device_id, operating_system, OS_patch_date
FROM machines;

SELECT event_id, country
FROM log_in_attempts;

SELECT username, login_date, login_time
FROM log_in_attempts;

SELECT *
FROM log_in_attempts;

SELECT *
FROM log_in_attempts
ORDER BY login_date;

SELECT *
FROM log_in_attempts
ORDER BY login_date, login_time;
```
