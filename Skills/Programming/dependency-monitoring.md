---
type: reference
title: Generalized Skill - Dependency Monitoring
description: A reusable pattern for detecting missing files, broken paths, and missed automation runs.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Dependency monitoring

Check whether a workflow's registered requirements remain usable and whether its
checks continue to run. Generalized utility pattern; no registry or monitoring service is included.

## Inputs

A dependency registry, expected cadence, grace periods, and an authorized alert destination.

## Workflow

1. Register required inputs, executables, output locations, and known consumers.
2. Check existence, readability, cloud-placeholder state, and relevant integrity
   conditions. Test permissions in the account that actually runs the workflow.
3. Before a proposed move, report registered consumers that would be affected.
   A move audit neither moves files nor discovers every dynamic dependency.
4. Save a timestamped local result. Send only a minimal success/failure signal
   to an independent heartbeat service.
5. Detect failures, started-but-unfinished runs, and missing runs. Preserve the
   distinction between dependency health and successful business output.
6. Verify a controlled failure and recovery before relying on alerts. Obtain
   required approval before activating schedules or sending external test alerts.

## Output

A local dependency report, move-impact findings, and verified alert state.

## Adapt before use

Implement the registry and checks; configure scheduling, private heartbeat endpoints,
and alerts. Keep file contents and local paths out of external heartbeat payloads.
