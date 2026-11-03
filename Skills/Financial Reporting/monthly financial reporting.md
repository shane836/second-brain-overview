---
type: reference
title: Generalized Skill - Monthly Financial Reporting
description: A reusable pattern for preparing a validated monthly investor-reporting workbook.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Monthly financial reporting

Prepare a monthly reporting package from validated source documents.
Generalized skill reference; client templates, cell mappings, delivery configuration,
and reporting integrations are not included.

The [Monthly Financial Reporting code package](https://github.com/shane836/monthly-financial-reporting)
contains sanitized workbook, email, delivery-tracking, and monitoring helpers,
with fictional examples and tests. It requires environment-specific adaptation.

## Inputs

The reporting period, required source package, approved template, mapping rules,
prior-period context, and delivery history.

## Workflow

1. Confirm the period and check prior delivery state to avoid duplicate packages.
2. Verify that all required financial and operating inputs are readable,
   complete, and dated for the intended period. Report missing inputs explicitly.
3. Calculate year-to-date and month-end figures from actual source dates.
   Reconcile financial subtotals and operating counts independently.
4. Resolve differences through evidence. Never force a balancing adjustment or
   inherit a historical exception without confirming its amount and cause.
5. Write approved inputs to a template copy with provenance for every value.
   Preserve formulas, history, hidden sheets, formatting, and other workbook features.
6. Recalculate with a compatible engine and inspect the saved final workbook.
   Stale formula caches do not establish verified results.
7. Prepare the review package. Deliver only within the authorized scope;
   track confirmed delivery separately from attempts and reporting completion.

## Output

A completed workbook, validation report, source mapping, and verified delivery state.

## Adapt before use

Obtain the recipient's template and mappings, define tolerances and exception
handling, and test the workbook-preservation and recalculation path. Treat missing
inputs and missed runs as explicit failure states.
