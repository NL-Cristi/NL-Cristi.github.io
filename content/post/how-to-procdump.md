+++
title = "How to Procdump??"
date = 2022-11-30T00:00:00+08:00
description = "Easy how to use Procdump"
tags = ["Generic"]
aplayer = false
showLicense = false
+++

Please replace ***999*** from the lower table with the PID of your process. To get the pid you can use the Details View of the TaskManager or powershel/cm.

# | Scenario | Objective | Basic syntax |
--- |--- |--- |--- |
|1|**Hang** dump |Creates a dump file (process memory is saved to disk) when the tool runs |```.\procdump.exe -ma 999```|
|2|**Crash** dump|Monitors a process and creates a dump file when the process runs into an unhandled exception|```.\procdump.exe -ma -e 999```|
|3|Dump on **exception**|Monitors a process and creates a dump file on a specific exception (i.e. any exceptions of form *ArgumentNullException*)|```.\procdump.exe -ma -e 1 -f ArgumentNullException 999```|
|4|Dump on **first chance exception**|Monitors a process and creates a dump file on a first chance exception|```.\procdump.exe -ma -e 1 999```|
|5|**Monitors exceptions**|Monitors a process for exceptions without taking a dump |```.\procdump.exe -ma -e 1 -f "" 999```|
|6|Dump on **performance trigger**|Monitors a process and takes a hang dump when a performance trigger is hit|```.\procdump.exe -ma -p <Counter> <Threshold value> <process name or service or PID>```|

