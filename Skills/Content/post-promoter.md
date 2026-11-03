---
type: reference
title: Generalized Skill - Post Promoter
description: A reusable pattern for reviewed promotion with recipient qualification and delivery tracking.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Post promoter

Prepare and track promotion of an existing published post or article using an AI agent to send approved messages and an AI native CRM like Attio to manage duplicates and track outreach status.. Generalized
skill reference; no contacts, messages, CRM configuration, or sending schedule is included.

## Inputs

A verified live URL, campaign objective, proposed copy, audience criteria,
exclusions, delivery history, and a campaign end condition.

## Workflow

1. Present exact messaging, qualification criteria, destinations, and proposed
   timing for approval before sending or activating a schedule.
2. Verify recipients and relevant group rules. Reconcile prior conversations,
   opt-outs, and cross-campaign history before determining eligibility.
3. Define recontact rules explicitly. A new campaign must not silently reset
   exclusions, cooldowns, or an unresolved prior delivery.
4. Save queue state before each attempt, using a unique campaign/channel/destination
   key so resumed or concurrent runs do not send duplicates.
5. Mark success only with native delivery evidence. Keep pending moderation,
   uncertain delivery, and failure distinct; reconcile uncertainty before retrying.
6. Report confirmed results and remaining work. Stop at the agreed end condition
   or on an account warning, access restriction, or loss of reliable state.

## Output

An approved campaign plan and a reconciled delivery ledger.

## Adapt before use

Supply a verified ledger, supported sending methods, recipient permissions,
platform requirements, recontact policy, and operational limits. No quotas or
timing preferences from a private campaign are carried into this reference.
