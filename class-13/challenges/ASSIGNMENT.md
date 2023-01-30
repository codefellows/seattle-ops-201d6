# Ops Challenge - Domain Analyzer

## Overview

Public domain information can be a liability when defending something like a web server against cyber attack. Shell scripts can be useful tools in automating the gathering of useful intelligence about a domain for both offensive and defensive purposes. Today you'll add a new function to your admin tool that fetches domain information for a given input.

## Objectives

- Create a script that asks a user to type a domain, then displays information about the typed domain. Operations that must be used include:
  - `whois`
  - `dig`
  - `host`
  - `nslookup`

## Resources

- [How to Use the whois Command on Linux](https://www.howtogeek.com/680086/how-to-use-the-whois-command-on-linux/)

## Tasks

Install `whois` on your Ubuntu VM.

Add to your bash script a sixth option that calls a function to:

- Take a user input string. Presumably the string is a domain name such as Google.com.
- Run `whois` against a user input string.
- Run `dig` against the user input string.
- Run `host` against the user input string.
- Run `nslookup` against the user input string.

Output the results to a single .txt file and open it with your favorite text editor.

For this challenge you must use at least one variable and one function.

## Stretch Goals (Optional Objectives)

Pursue these optional objectives if you have additional remaining lab time or are an advanced shell scripter.

- Check that the input is a valid domain name.
- Research and add additional tools that fetch domain information to your shell script.
- Sanitize the output to only display useful information.

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
