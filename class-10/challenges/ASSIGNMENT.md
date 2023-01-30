# Ops Challenge - System Process Commands

## Overview

In today's Ops Challenge you will analyze, initialize, and terminate processes (programs) using Powershell commands. As you practice these commands and gain skill with Powershell scripting, consider both the administrator utility value and cyber attacker utility value of knowing such commands.

## Feature Tasks and Requirements

Create a Powershell script that performs these operations on separate lines. The overall script is not designed to operate holistically, but rather act as a reference for how to execute various interesting operations with the process family of Powershell commandlets. Clearly indicate with comments each component below.

  1. Print to the terminal screen all active processes ordered by highest CPU time consumption at the top.
  1. Print to the terminal screen all active processes ordered by highest Process Identification Number at the top.
  1. Print to the terminal screen the top five active processes ordered by highest Working Set (WS(K)) at the top.
  1. Start the process Internet Explorer (iexplore.exe) and have it open https://owasp.org/www-project-top-ten/.
  1. Start the process Internet Explorer (iexplore.exe) ten times using a for loop. Have each instance open https://owasp.org/www-project-top-ten/.
  1. Close all Internet Explorer windows.
  1. Kill a process by its Process Identification Number. Choose a process whose termination won't destabilize the system, such as Internet Explorer or MS Edge.

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
