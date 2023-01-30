# Pipelines

Pipelines, often called pipes, is a way to chain commands and connect output from one command to the input of the next.

A pipeline is represented by the pipe character: `|`. It's particularly handy when a complex or long input is required for a command.

    command1 | command2

By default pipelines redirects only the standard output, if you want to include the standard error you need to use the form `|&` which is a short hand for `2>&1 |`.

## Example

Imagine you quickly want to know the number of entries in a directory, you can use a pipe to redirect the output of the `ls` command to the `Measure-Object` command with option `-Line`.

    ls \ | Measure-Object -Line

Then you want to see only the first 10 results

    ls \ | select -First 10


`select-String` searches for patterns in each file. Patterns is one or more patterns separated by newline characters, and Select-String prints each line that matches a pattern. Typically patterns should be quoted when Select-String is used in a PowerShell command.

    ls / | Select-String  # This will grab any line/file that has a matching pattern in it

## Exercise

In this exercise, you will need to print the number of processors based on the information from the `systeminfo` command

*Hint 1: each processor has a unique number, for instance the first processor will contain the line ``processor: 0``*

*Hint 2: you can chain together more than two commands in a row*

### Tutorial Code

    systeminfo |

### Expected Output

    8

*Note* - This result might change depending of your system specs.

### Solution

```powershell
systeminfo | Select-String "processor" | Measure-Object -Line
```
*Adapted from learnshell.org*
