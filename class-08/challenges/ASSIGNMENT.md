# Ops Challenge - Windows Batch Scripting

It could be said that batch scripts are to Windows as bash scripts are to Linux. If you're using basic Windows terminal commands (non-Powershell), then a .bat file is the way to go!

## Scenario

Jorge Thompson in marketing submitted a new service request today:
- Jorge writes: "Hello IT team, thanks so much for setting up my new internal hard drive last week. It works great, and I've been manually copying my work files on the desktop every night before I head home. I was curious if there's a way to automate this process? Just curious, thanks again!"

System credentials:
- Admin: admin / solarwinds123
- User(local): j.thompson / iceman456

## Objectives

- Automate the copy operation for Jorge

## Resources

- [How to Use Windows Batch File Commands to Automate Repetitive Tasks](https://www.makeuseof.com/tag/use-windows-batch-file-commands-automate-repetitive-tasks/){:target="_blank"}
- [Wikibooks: Windows Batch Scripting](https://en.wikibooks.org/wiki/Windows_Batch_Scripting){:target="_blank"}

## Tasks

### Part 1: Staging

If you followed the instructions from class 4's lab assignment, you should still have ops201-class04.ova installed in VirtualBox. You'll need that system for today.

### Part 2: Write a Batch File

Create a batch file that recursively copies Jorge's work files on his desktop (recursively meaning to include folder contents). 
- Your script should use `ROBOCOPY` as the primary means of copying the data.

### Part 3: Schedule the Task

Schedule a Windows task to execute this batch file every night at midnight.

## Stretch Goals (Optional Objectives)

Have your batch file generate a log file of what took place.

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
