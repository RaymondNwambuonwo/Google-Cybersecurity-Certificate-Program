# Managing Files with Linux Commands

## In this lab activity, we use Linux commands to modify a directory structure and the files it contains. As well as use the nano text editor to add text to a file

### Scenario

In this scenario, you need to ensure that the `/home/analyst` directory is properly organized. You have to make a few changes to the `/home/analyst` directory and the files it contains. You also have to edit a file to record the changes or updates you make to the directory.

### Description

Here’s how you’ll do this: First, you’ll create a new subdirectory called `logs` in the `/home/analyst` directory. Next, you’ll remove the `temp` subdirectory. Then, you’ll move the `Q3patches.txt` file to the `reports` subdirectory and delete the `tempnotes.txt` file. Finally, you’ll create a new `.txt` file called `tasks` in the `notes` subdirectory and add a note to the file describing the tasks you've performed.

```bash
mkdir logs
rmdir temp
mv Q3patches.txt /home/analyst/reports/
rm tempnotes.txt
touch tasks.txt
nano tasks.txt
cat tasks.txt
```
