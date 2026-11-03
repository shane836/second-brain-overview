---
type: reference
title: Generalized Skill - Article Adapter
description: A reusable pattern for adapting a source newsletter into a reviewed native article.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Article adapter

Adapt supplied newsletter articles to LinkedIn using Chat GPT Comnputer use. 
Generalized skill reference; publishing integrations are not included.

## Inputs

The complete source, images, publishing identity, editorial requirements, and
an optional target publication window.

## Workflow

1. Read the full source. Preserve the author's claims, qualifications, voice,
   and links; separate substantive corrections from formatting changes.
2. Inspect existing drafts and schedules before creating another draft.
3. Adapt headings, spacing, lists, and images for the destination platform.
4. Preview the saved article and verify that the beginning, sections, ending,
   and assets persist. Obtain the actual review link.
5. Present the finished article, announcement copy, proposed time, and material
   changes for approval. Check the publishing queue for duplicate announcements.
6. After approval, use a supported publication method and verify the saved state.
   A review link, editor URL, and live article URL are different artifacts.
7. Pass verified live URLs to promotion separately; publication approval does
   not authorize outreach.

## Output

A reviewable draft and change notes; after authorized publication, verified live links.

## Adapt before use

Supply account access, platform controls, editorial standards, timezone, capacity
rules, and an activity ledger. Do not inherit another author's publishing preferences.
