<!---
Copyright (C) 2024, Openarmor .
Created by Openarmor, . <info@openarmor.com>.
This program is free software; you can redistribute it and/or modify it under the terms of GPLv2
-->

# Centralized Configuration
## Index
- [Centralized Configuration](#centralized-configuration)
  - [Index](#index)
  - [Purpose](#purpose)
  - [Sequence diagram](#sequence-diagram)

## Purpose

One of the key features of Openarmor as a EDR is the Centralized Configuration, allowing to deploy configurations, policies, rootcheck descriptions or any other file from Openarmor Manager to any Openarmor Agent based on their grouping configuration. This feature has multiples actors: Openarmor Cluster (Master and Worker nodes), with `openarmor-remoted` as the main responsible from the managment side, and Openarmor Agent with `openarmor-agentd` as resposible from the client side.


## Sequence diagram
Sequence diagram shows the basic flow of Centralized Configuration based on the configuration provided. There are mainly three stages:
1. Openarmor Manager Master Node (`openarmor-remoted`) creates every `remoted.shared_reload` (internal) seconds the files that need to be synchronized with the agents.
2. Openarmor Cluster as a whole (via `openarmor-clusterd`) continuously synchronize files between Openarmor Manager Master Node and Openarmor Manager Worker Nodes
3. Openarmor Agent `openarmor-agentd` (via ) sends every `notify_time` (ossec.conf) their status, being `merged.mg` hash part of it. Openarmor Manager Worker Node (`openarmor-remoted`) will check if agent's `merged.mg` is out-of-date, and in case this is true, the new `merged.mg` will be pushed to Openarmor Agent.