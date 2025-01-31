# Input/Output in the Linux shell

## This lab consists of using the `echo` command to examine how input is received and how output is returned in the shell. Next, using the `expr` command to further explore input and output while performing some basic calculations in the shell

### Scenario

As a security professional, it’s important to understand the concept of communicating with your computer via the shell.

In this scenario, you have to input a specified string of text that you want the shell to return as output. You'll also need to input a few mathematical calculations so the OS (operating system) can return the result.

Here’s how you’ll do this: First, you’ll use the echo command to generate some output in the shell. Second, you’ll use the expr command to perform basic mathematical calculations. Next, you’ll use the clear command to clear the Bash shell window. Finally, you’ll have an opportunity to explore the echo and expr commands further.

Get ready to examine input and output in the Bash shell!

```bash
echo hello

echo "hello"
Note: The output is the same as before. The quotation marks are optional in this case, but they tell the shell to group a series of characters together. This can be useful if you need to pass a string that contains certain characters that might be otherwise misinterpreted by the command.

expr 32 - 8
Note: The expr command requires that all terms and operators in an expression are separated by spaces. For example: expr 32 - 8, and not expr 32-8.

clear
Note: All previous commands and output will be cleared, and the user prompt and cursor will return to the upper left of the shell window.

Note: The expr command performs integer mathematical calculations only, so you cannot use the decimal point or expect a fractional result. All results are rounded down to the nearest integer. Also, all terms and operators in an expression need to be separated by spaces. For example: expr 25 + 15, and not expr 25+15.
```
