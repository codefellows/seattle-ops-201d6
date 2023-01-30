# Ops Challenge - Log Retrieval via Powershell

## Overview

Powershell can be a powerful time saving tool for common tasks like accessing or backing up system logs. In today's Ops Challenge you'll get to write scripted commands that retrieve system log information via Powershell instead of Event Viewer.

## Objectives

- Create a Powershell script that fetches useful System event logs.

## Resources

- [Microsoft.PowerShell.Management documentation](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/?view=powershell-5.1)

## Tasks

- Output all events from the System event log that occurred in the last 24 hours to a file on your desktop named last_24.txt.
- Output all "error" type events from the System event log to a file on your desktop named errors.txt.
- Print to the screen all events with ID of 16 from the System event log.
- Print to the screen the most recent 20 entries from the System event log.'
- Print to the screen all sources of the 500 most recent entries in the System event log. Ensure that the full lines are displayed (get rid of the ... and show the entire text).

> Remember to follow this class's commenting requirements on all scripts.

## Stretch Goals (Optional Objectives)

Pursue these optional objectives if you are an advanced Powershell user or have remaining lab time.

- Embed each task above into its own function, then call each function in main.
- Ensure that full lines are displayed in all tasks above, similar to task 5.

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
