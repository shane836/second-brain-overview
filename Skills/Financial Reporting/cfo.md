---
type: reference
title: Generalized Skill - CFO
description: A reusable pattern for orienting financial analysis around authoritative sources and traceable figures.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# CFO

Orient liquidity and spending analysis around documented systems of record.
Generalized skill reference; financial connectors, company mappings, and workbooks are not included.

To make this practically useful, you need to organize your financial records and connect an accounting system. I connected Quickbooks via O-Auth. 

## Inputs

The question, entity scope, reporting period, source register, and authorized
statements or ledger extracts.

## Workflow

1. Read the current systems reference and prior decisions before rebuilding
   integrations or deriving figures.
2. Identify the authoritative source for each figure, its entity, period,
   accounting basis, and source freshness.
3. Reconcile relevant records. Distinguish spending from transfers, borrowing,
   capital movements, and withdrawals; cash movement alone is not an expense.
4. Recompute figures for the requested period. Flag gaps and stale books rather
   than filling them with unsupported estimates.
5. Work on copies of financial models. Preserve originals and verify that
   formulas, embedded objects, and workbook features survive the chosen tools.
6. Return traceable findings and unresolved differences. Prepare proposed
   corrections separately from any authorized posting or external action.
7. Save durable decisions and a handoff for the next session.

## Output

Period-specific analysis, source provenance, reconciliations, and explicit limitations.

## Adapt before use

Supply the entity/source map, connectors, credentials through private configuration,
classification rules, and review boundaries. No private account structure is implied.
