# Filter SQL queries

## In this lab activity, you’ll apply these operators to accurately filter for specific numbers and dates

Common operators for working with numeric or date and time data will help you accurately filter data. These are some of the operators you'll use:

```bash
= (equal)
> (greater than)
< (less than)
<> (not equal to)
>= (greater than or equal to)
<= (less than or equal to)
```

### Scenario

In this scenario, you’re investigating a recent security incident. You need to gather information about login attempts for certain dates and times. This will help in resolving a security incident. Here’s how you’ll do this task: First, you’ll retrieve login events made after a certain date. Second, you’ll narrow the focus of the search to filter logins in a date range. Third, you’ll investigate logins that were made at certain times. Finally, you’ll filter login attempts based on their event IDs.

```SQL
SELECT * FROM
log_in_attempts
WHERE login_date > '2022-05-09';

SELECT *
FROM log_in_attempts
WHERE login_date >= '2022-05-09';

SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2022-05-09' AND '2022-05-11';

SELECT *
FROM log_in_attempts
WHERE login_time < '07:00:00';

SELECT *
FROM log_in_attempts
WHERE login_time BETWEEN '06:00:00' AND '07:00:00';

SELECT event_id, username, login_date
FROM log_in_attempts
WHERE event_id >= 100;

SELECT event_id, username, login_date
FROM log_in_attempts
WHERE event_id BETWEEN 100 AND 150;
```
