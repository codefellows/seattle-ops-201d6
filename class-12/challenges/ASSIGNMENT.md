# Ops Challenge - Powershell IP Analysis

## Overview

In today's challenge you will meet Powershell's own version of Linux's `grep` command: `Select-String`. This can be used to filter your Powershell outputs and search files or folders for text patterns.

## Objectives

- Write a Powershell script that returns the IPv4 address of the computer.
- Use `Select-String` cmdlet to only return the IPv4 address string and no other extraneous information.

## Resources

- [Select-String](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/select-string?view=powershell-7.1)

## Tasks

Create a Powershell script that performs the following operations:
- Create a local file called network_report.txt that holds the contents of an `ipconfig /all` command.
- Use `Select-String` to search network_report.txt and return only the IP version 4 address.
- Remove the network_report.txt when you are finished searching it.

For this challenge, you must use at least one variable and one function.

## Stretch Goals (Optional Objectives)

- Instead of creating network_report.txt, use piping to store the output in memory and search it there.
- Have your script test whether the network adapter is sending and receiving packets correctly.
- Have your script test connectivity to the internet

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
