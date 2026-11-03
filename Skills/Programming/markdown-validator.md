---
type: reference
title: Generalized Skill - Markdown Validator
description: A reusable pattern for checking Markdown metadata without rewriting notes.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Markdown validator

Check whether knowledge notes satisfy a defined metadata schema. Generalized
utility pattern; validator code and agent-hook configuration are not included.

## Inputs

A vault root, required fields, allowed values, workflow rules, and exclusions.

## Workflow

1. Restrict validation to intended Markdown notes. Exclude dependencies, native
   instruction files, and symlinks leading outside the authorized scope.
2. Parse frontmatter safely. Reject malformed YAML and duplicate keys.
3. Check required nonempty fields, allowed lifecycle values, and navigation fields.
4. Keep document lifecycle separate from workflow. Apply the appropriate workflow
   field for the note's workstream; omit it when no workflow applies.
5. Return field-specific errors without modifying the note.
6. Check changed notes during ordinary edits. Provide an explicit whole-vault
   audit without letting unrelated legacy errors block every agent interaction.

## Output

A count of checked notes, specific validation errors, and an unambiguous result.
Schema validity does not prove that a note's facts are correct.

## Adapt before use

Define the schema and exception rules first. Implement and test the validator,
then wire only supported hook events. Verify hook activation in the actual host;
configuration alone does not prove that enforcement runs.
