# Using Grep

## In this lab activity, I use the grep command and piping to search for files and to return specific information from files via the command line

### Scenario

In this scenario, you need to obtain information contained in server log and user data files. You also need to find files with specific names.

Here’s how you’ll do this: First, you’ll navigate to the logs directory and return the error messages in the server_logs.txt file. Next, you’ll navigate to the users directory and search for files that contain a specific string in their names. Finally, you’ll search for information contained in user files.

```bash
grep error server_logs.txt

ls | grep Q1

ls | grep access

grep jhill Q2_deleted_users.txt

grep "Human Resources" Q4_added_users.txt
```
