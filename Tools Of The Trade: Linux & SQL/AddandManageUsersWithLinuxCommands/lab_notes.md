# Add and manage users with Linux commands

## In this lab activity, I use the `useradd`, `usermod`, `userdel`, and `chown` commands to manage user access in the Linux Bash shell

### Scenario

In this scenario, a new employee with the username researcher9 joins an organization. You have to add them to the system and continue to manage their access during their time with the organization.

Here’s how you’ll do this task: First, you’ll add a new employee to the system and then to their primary group. Second, you’ll make this employee the owner of a file related to a particular project. Third, you’ll add the new employee to a supplementary group. Finally, you’ll delete the employee from the system.

> **Note:** When you create a new user in Linux, a group with the same name as the user is automatically created and the user is the only member of that group. After removing users, it is good practice to clean up any such empty groups that may remain behind.

```bash
sudo groupdel researcher9
sudo useradd researcher9
sudo usermod -g research_team researcher9
sudo useradd researcher9 -g research_team
sudo chown researcher9 /home/researcher2/projects/project_r.txt
sudo usermod -a -G sales_team researcher9
sudo userdel researcher9
sudo groupdel researcher9
```
