<!---
Copyright (C) 2024, Openarmor .
Created by Openarmor, . <info@openarmor.com>.
This program is free software; you can redistribute it and/or modify it under the terms of GPLv2
-->

# Metrics

## Index

- [Metrics](#metrics)
  - [Index](#index)
  - [Purpose](#purpose)
  - [Sequence diagram](#sequence-diagram)

## Purpose

Openarmor ludes some metrics to understand the behavior of its components, which allow to investigate errors and detect problems with some configurations. This feature has multiple actors: `openarmor-remoted` for agent interaction messages, `openarmor-analysisd` for processed events.

## Sequence diagram

The sequence diagram shows the basic flow of metric counters. These are the main flows:

1. Messages received by `openarmor-remoted` from agents.
2. Messages that `openarmor-remoted` sends to agents.
3. Events received by `openarmor-analysisd`.
4. Events processed by `openarmor-analysisd`.
