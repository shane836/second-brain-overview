---
type: reference
title: Generalized Skill - Folder Sorting
description: A reusable pattern for sorting Markdown notes into folders using workstream metadata.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Folder sorting

Organize active Markdown notes by their `workstream` property. Generalized utility
pattern; no sorting script or private folder map is included.

## Inputs

A notes root, a workstream-to-folder map, and the set of references to inspect.

## Workflow

1. Read frontmatter and map each recognized workstream to its destination.
2. Prepare a move manifest. Flag missing metadata, unknown workstreams, and
   destination collisions; do not guess classifications or overwrite files.
3. Preserve a recovery record before moving notes within the authorized scope.
4. Move eligible notes and record actual outcomes. A skipped collision must not
   be counted as a successful move.
5. Update affected path references within the defined scope. Verify links after
   moving; basename links and literal file paths can behave differently.
6. Rerun the inventory and report remaining exceptions.

## Output

A move report, reference changes, and unresolved notes. Rerunning should leave
already-organized notes in place.

## Adapt before use

Supply the folder map, metadata parser, link conventions, and recovery method.
The original pattern updates selected known references; a general link scanner
would be additional implementation work, not an included capability.
