<!---
Copyright (C) 2024, Openarmor .
Created by Openarmor, . <info@openarmor.com>.
This program is free software; you can redistribute it and/or modify it under the terms of GPLv2
-->

# Openarmor module: CIS-CAT architecture
## Index
- [Openarmor module: CIS-CAT architecture](#openarmor-module-cis-cat-architecture)
  - [Index](#index)
  - [Purpose](#purpose)
  - [Sequence Diagram](#sequence-diagram)

## Purpose
The **CIS-CAT** Openarmor module integrates CIS benchmark assessments into Openarmor agents and reports the results of each scan in the form of an alert. The module requires the use of **CIS-CAT Pro**, an external tool developed for scanning target systems and generating a report comparing the system settings to the CIS benchmarks.

## Sequence Diagram
The provided sequence diagram shows the basic flow of Openarmor's **CIS-CAT** module. The main steps are:

1. The **CIS-CAT** module is executed according to the configuration provided in `ossec.conf`.
2. The **CIS-CAT** module runs the scan every defined interval.
3. The script scans the system and reports the results trough different files (**txt** and **xml**).
4. The **txt** file is parsed. The relevant information from this file is stored in memory (mostly `scan_info`). 
5. The **xml** file is parsed. The relevant information from this file is stored in memory (`rule_info`).
6. Once we have all the information (both generic and specific), we convert the data to a **JSON** structure to send the stored information to the manager.
7. Once the data is sent, the generated reports are removed and the used memory is freed for the next scan.
