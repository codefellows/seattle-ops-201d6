# Ops Challenge - Powershell IP Analysis

Here are the tools needed for today's Ops Challenge. Most notably we're using `Select-String` and functions for the first time.

## Demo Code

```powershell
# Script Name: Demo Ops 201 Class 12
# Author: David Lee
# Date of last revision:
# Purpose: Demo tools used in today's Ops Challenge

### REVIEW ###

# How to view network configuration of this computer's network adapters
ipconfig /all

# How to test internet connectivity
ping google.com

# How to verify this network adapter is sending and receiving signals
ping 127.0.0.1

# Variable declaration and call
$target = "google.com"
ping $target

### NEW TOOLS ###

# How to use the Select-String cmdlet

# Select-String -Path [literal file path] -Pattern [pattern to search for]

# First, create a file
ping google.com > "ping_test.txt"

# Then run Select-String to search for a pattern
echo "Pinging Google.com..."
Select-String -Path "ping_test.txt" -Pattern 'Packets:'

# If you are testing this frequently, remove the .txt file afterwards
rm "ping_test.txt"

# How to declare and call a function in Powershell
Function Do-Stuff {
  echo "I'm doing stuff!"
}

Do-Stuff

# What's so great about functions? Do LOTS of stuff in a single function.
Function Do-More-Stuff {
  echo "I'm doing stuff!"
  echo "I'm doing more stuff like pinging google.com! Watch:"
  ping google.com
}

Do-More-Stuff

# We can put variables inside of functions to add complexity
Function Do-More-Stuff-Using-Variables {
  $target = "google.com"
  echo "I'm doing stuff with functions and variables!"
  echo "I'm doing more stuff like pinging google.com! Watch:"
  ping $target
}

Do-More-Stuff-Using-Variables
```
