# Add and manage users with Linux commands

## In this lab activity, I use the `man` and `whatis` commands to get information on other commands and how they work. I’ll also use the `apropos` command to search the manual page for a command with a specified string

### Scenario

In this scenario, you have to find more information about commands that you need to use. You also need to discover which command to use to perform a certain task.

Here’s how you’ll do this task: First, you’ll explore a few commands you can use in the shell to learn more about other commands. Next, you’ll find an option you need to add to a command. Third, you’ll use a command to get a brief description of commands so you can identify their differences. Finally, you’ll identify the command you need to perform a task.

> **Note:** There is no right and wrong when using `apropos` in terms of keywords. Think of it as a very focused search. It will only return commands that correspond to keywords you supply. Keep trying if the first returned command does not provide what you need. Also, keep in mind that using the `-a` option will limit results to only those commands that match all keywords supplied.

```bash
whatis cat
man cat
apropos -a first part file
man useradd
apropos -a create new group
```
