# Ops Challenge - Log Retrieval via Powershell

## Overview

Powershell can be a powerful time saving tool for common tasks like accessing or backing up system logs. In today's Ops Challenge you'll get to write scripted commands that retrieve system log information via Powershell instead of Event Viewer.

## Feature Tasks and Requirements

For the below tasks, reference the official [Microsoft.PowerShell.Management documentation](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/?view=powershell-5.1) for the appropriate syntax.

- **Task 1**: Output all events from the System event log that occurred in the last 24 hours to a file on your desktop named last_24.txt.

- **Task 2**: Output all "error" type events from the System event log to a file on your desktop named errors.txt.

- **Task 3**: Print to the screen all events with ID of 16 from the System event log.

- **Task 4**: Print to the screen the most recent 20 entries from the System event log.'

- **Task 5**: Print to the screen all sources of the 500 most recent entries in the System event log. Ensure that the full lines are displayed (get rid of the ... and show the entire text).

For all Ops Challenge scripts in this class, add the below information as comments:

- Script Name
- Author
- Date of last revision
- Description of purpose
- Declaration of variables
- Declaration of functions (if used)
- Main
- End

## Stretch Goals (Optional Objectives)

Pursue these optional objectives if you are an advanced Powershell user or have remaining lab time.

- Embed each task above into its own function, then call each function in main.
- Ensure that full lines are displayed in all tasks above, similar to task 5.

## Submission Instructions

- When you are ready to submit your shell script for grading, copy your script from Ubuntu VM Terminal to a new **public** GitHub Gist.
- Copy the URL to your Gist and paste below as your submission.
