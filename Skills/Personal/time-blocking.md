---
type: reference
title: Generalized Skill - Time Blocking
description: A reusable pattern for building reviewable calendar plans around commitments and task priorities.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Time blocking

Turn a task list into a feasible calendar plan. Generalized skill reference;
calendar access and personal scheduling preferences are not included.

## Inputs

The planning dates, timezone, working hours, fixed commitments, priorities,
duration estimates, and preferred focus or meeting windows.

## Workflow

1. Read the current calendar through an authorized interface. Inspect dates,
   timezone, all-day events, busy status, and recurrence before placing blocks.
2. Preserve fixed commitments and any changes the user has already made.
3. Allocate priority work within real availability, including transitions,
   breaks, and task dependencies. Surface work that cannot fit.
4. Present the finished plan with proposed moves and unresolved conflicts.
   Do not silently inherit another person's preferred hours or meeting pattern.
5. Before applying approved changes, reread the calendar and reconcile
   intervening edits. Change only the authorized events and recurrence scope.
6. Read back saved events and report the actual dates, times, and remaining conflicts.

## Output

A reviewable plan; after authorized calendar edits, a verified schedule.

## Adapt before use

Supply a calendar connector, availability rules, timezone handling, conflict
policy, and approval requirements. Use a test calendar for implementation checks.
