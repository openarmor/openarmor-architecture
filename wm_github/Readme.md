<!---
Copyright (C) 2024, Openarmor .
Created by Openarmor, . <info@openarmor.com>.
This program is free software; you can redistribute it and/or modify it under the terms of GPLv2
-->

# Openarmor module: Github architecture
## Index
1. [Purpose](#purpose)
2. [Sequence Diagram](#sequence-diagram)
3. [Findings](#findings)

## Purpose
Github infrastructure resources provides a several set of audit logs. The audit log allows organization admins to quickly review the actions performed by members of the organization. It ludes details such as who performed the action, what the action was, and when it was performed.

Openarmor has the ability to obtain and process Github audit log through:
- Github module

## Sequence Diagram
Sequence diagram shows the basic flow of Openarmor Github integration based on the configuration provided. Steps are:
1. Setup the Github module based on the configuration information, set organization name and token.
2. Generate a request with configuration information.
3. Execute the request.
4. Process answered request and audit logs.
5. Insert events into openarmor DB.


## Findings
* Sensitive information can be detected (token) into ossec.conf file, because is used as a plain text without obfuscation. This can lead to potential attacks and information theft.