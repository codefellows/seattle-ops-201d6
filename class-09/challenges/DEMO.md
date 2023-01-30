# Challenge - Powershell Logs

Today we're practicing the Get-EventLog commandlet in Powershell.

## Demo Code

```
# Script Name: Demo Ops 201 Class 09
# Author: David Lee
# Date of last revision:
# Purpose: Demo

# Declare variables
# Declare functions
# Main

# Get event logs on the local computer

Get-EventLog -List

# Get recent entries from an event log on the local computer

Get-EventLog -LogName System -Newest 5

# Find all sources for a specific number of entries in an event log

$Events = Get-EventLog -LogName System -Newest 1000
$Events | Group-Object -Property Source -NoElement | Sort-Object -Property Count -Descending

# Get error events from a specific event log

Get-EventLog -LogName System -EntryType Error

# Get events from an event log using a source and event ID

Get-EventLog -LogName Application -Source Outlook | Where-Object {$_.EventID -eq 63} |
              Select-Object -Property Source, EventID, InstanceId, Message

#End
```
