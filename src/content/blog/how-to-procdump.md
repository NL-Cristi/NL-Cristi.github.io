---
author: Cristian Negulescu
pubDatetime: 2022-12-04T09:30:41.816Z
modDatetime: 2024-01-04T09:30:41.816Z
title: How to procdump
slug: "how-to-procdump"
featured: true
draft: false
ogImage: ../../assets/images/AstroPaper-v4.png
tags:
  - dumps
  - windbg
  - procdump
description: "Some rules & recommendations for creating or adding new posts using AstroPaper
  theme."
---
Use this for an easy way of when/how to use procdump

Please replace ***999*** from the lower table with the PID of your process. To get the pid you can use the Details View of the TaskManager or powershel/cm.



|#|Scenario|Objective|Basic syntax|
|---|---|---|---|
|1|**Hang** dump |Creates a dump file (process memory is saved to disk) when the tool runs |```.\procdump.exe -ma 999```|
|2|**Crash** dump|Monitors a process and creates a dump file when the process runs into an unhandled exception|```.\procdump.exe -ma -e 999```|
|3|Dump on **exception**|Monitors a process and creates a dump file on a specific exception (i.e. any exceptions of form *ArgumentNullException*)|```.\procdump.exe -ma -e 1 -f ArgumentNullException 999```|
|4|Dump on **first chance exception**|Monitors a process and creates a dump file on a first chance exception|```.\procdump.exe -ma -e 1 999```|
|5|**Monitors exceptions**|Monitors a process for exceptions without taking a dump |```.\procdump.exe -ma -e 1 -f "" 999```|
|6|Dump on **performance trigger**|Monitors a process and takes a hang dump when a performance trigger is hit|```.\procdump.exe -ma -p <Counter> <Threshold value> <process name or service or PID>```|
