---
type: reference
title: Generalized Skill - Handoff
description: A reusable pattern for preserving session context so another agent can resume a task.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Handoff

Write a briefing that lets another agent resume work without replaying the
conversation. Generalized skill reference; no vault-specific installation is included.

## Inputs

The session's evidence, relevant project notes, an existing workstream hub, and
the receiving vault's metadata rules.

## Workflow

1. Separate completed and verified work from attempts, proposals, and blocked work.
2. Read the relevant hub and existing handoff before writing a dated summary.
3. Capture current state, discoveries, settled decisions, unresolved work with
   owners, and durable lessons. Convert relative dates to absolute dates.
4. Add required metadata and links to the existing workstream. Keep document
   lifecycle separate from project or publishing progress.
5. Link the summary from the hub and reconcile stale hub statements with the
   verified outcome. Update durable project memory when necessary.
6. Validate metadata, destinations, and links. Report what changed and what remains.

## Output

A dated session note and an updated navigation hub. Preserve source references
needed to resume, but never embed credentials or secret values.

## Adapt before use

Choose the vault root, summary directory, hub conventions, metadata schema, and
validator. Session summaries remain private unless separately reviewed for sharing.
