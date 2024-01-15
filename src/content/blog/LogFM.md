---
author: Cristian Negulescu
pubDatetime: 2024-01-15T09:30:41.816Z
title: LogFM 
featured: true
draft: true
ogImage: ../../assets/images/GreenGenerateZip.jpg.png
tags:
  - logs
  - tool
description: "PowerShell tool created to ease log collection for IIS realated issues."
---
[LogCatcher]:https://github.com/NL-Cristi/LogCatcher

I'm a **LAZY** person so when i face scenarios where i have a bunch of logs i hate reviewing them indivitually.

On linux i can use **GREP** but its not easy to have other people do this or teach them to do this.

**SOLUTION**:

I wrote **LogFM** command-line application designed to process, format and/or filter log files generated.It supports various operations such as reading from a single file or a directory, outputting to a specific file or directory, and merging/filtering log files. 

***PREREQUISITE*** : The log should start with date time (**ex:** *2023-12-04 11:27:02.500*)