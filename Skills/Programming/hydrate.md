---
type: reference
title: Generalized Skill - Hydrate
description: A reusable pattern for making online-only cloud files readable by an agent.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Hydrate

Make selected online-only cloud files available locally before an agent reads them.
Generalized utility pattern; implementation and provider configuration are not included.

## Inputs

A selected folder, cloud provider, available disk space, and an optional dry run.

## Workflow

1. Survey only the requested scope. Identify placeholders through provider metadata;
   a zero-byte file alone does not establish whether it is empty or online-only.
2. Report the proposed downloads before a large hydration operation.
3. Use the provider's supported download mechanism. A plain read may work for
   dataless files but can return empty content for other placeholder systems.
4. Process bounded batches. Preserve documents the user already has open.
5. Recheck placeholder state and readability. Report unresolved files separately;
   a successful open request does not prove that a download finished.

## Output

Counts of already-local, downloaded, and unresolved files. Keep detailed local
paths in a local report rather than an external notification.

## Adapt before use

Implement provider detection, download requests, timeouts, and verification.
Some macOS download methods require a logged-in desktop session. Test with
disposable files, including an empty file and an actual online-only file.
