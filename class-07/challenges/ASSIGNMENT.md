# Ops Challenge - System Information

## Overview

When working on a new system or troubleshooting performance issues, a quick look at system information is a great starting point. Automating the gathering of useful information can dramatically expedite troubleshooting times for busy support technicians. In todays' challenge you will write a script that outputs a report about current system CPU and RAM performance of a Ubuntu Linux computer.

> If you're wondering how the same operation is done in Windows, that's instead going to involve Powershell, a separate language from Bash.

## Objectives

Create a script that...
  - Uses `lshw` to display system information to the screen about the following components:
    - Name of the computer
    - CPU
      - Product
      - Vendor
      - Physical ID
      - Bus info
      - Width
    - RAM
      - Description
      - Physical ID
      - Size
    - Display adapter
      - Description
      - Product
      - Vendor
      - Physical ID
      - Bus info
      - Width
      - Clock
      - Capabilities
      - Configuration
      - Resources
    - Network adapter
      - Description
      - Product
      - Vendor
      - Physical ID
      - Bus info
      - Logical name
      - Version
      - Serial
      - Size
      - Capacity
      - Width
      - Clock
      - Capabilities
      - Configuration
      - Resources
  - Uses `grep` to remove irrelevant information from the `lshw` output
  - Add text to the output clearly indicating which component (such as CPU, RAM, etc.) the script is returning information about
  - Runs as Root; you may execute the shell script with `sudo` or as Root

## Resources

- [Linux lshw Command Tutorial for Beginners](https://www.howtoforge.com/linux-lshw-command/){:target="_blank"}
- [How to use the Linux Grep Commmand](https://careerkarma.com/blog/linux-grep-command/){:target="_blank"}
- Tutorials
  - [Bash](demo/bash.md)
  - [PowerShell](demo/powershell.md)
  - [Z shell](demo/zsh.md)

## Stretch Goals (Optional Objectives)

Complete these optional objectives if you have extra lab time or are an advanced Linux user.

- Add BIOS information to your report using `dmidecode`. Run your script with `sudo` if necessary.
- Update the report title to include "BIOS".
- Create readable headers and spacing on the generated report.
- Add additional system information to the generated report using Linux commands you've learned so far in Ops 201. Be sure to organize the report title and headers, sorting information in a readable manner.

## Submission Instructions

Your instructional team will grade your assignment, and give you feedback.

Submit a link to your script file on your public GitHub repo.
