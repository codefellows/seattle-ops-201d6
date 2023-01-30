# Challenge - System Process Analysis

## Demo Code

```
# Script Name: Demo Ops 201 Class 10
# Author: David Lee
# Date of last revision:
# Purpose: Demo

# Declare variables
# Declare functions
# Main

# Reference https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/start-process?view=powershell-7

# Get a list of all active processes on the local computer

Get-Process

# Get all the Powershell processes in the current session

Get-Process pwsh

# Get all available data about one or more processes

Get-Process winword, explorer | Format-List *

# Sort the output of a commandlet by property

[commandlet] | Sort-Object -Property [property to sort by] -Descending

# How to initialize a process by its filepath

Start-Process -FilePath "C:\Program Files (x86)\Foxit Software\Foxit PhantomPDF\FoxitPhantomPDF.exe"

# For loop syntax

for ($i = 1 ; $i -le 5 ; $i++)
{
    echo "Loop iteration number $i"
}

# End
```
