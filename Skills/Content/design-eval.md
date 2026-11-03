---
type: reference
title: Generalized Skill - Design Evaluation
description: A reusable pattern for measuring rendered designs against explicit, calibrated criteria.
workstream: programming
hub: "[[Programming_Automation]]"
status: draft
---

# Design evaluation

Allow your agents to autonomously iterate on graphic design choices to improve the aesthetic quality of your firm's deliverables. Measure objective defects and identify subjective judgments separately. Generalized skill reference; measurement scripts, brand assets, and private rubrics are not included.

## Inputs

A renderable artifact, available source, intended audience and viewing conditions,
approved copy, and an agreed rubric or references for building one.

## Workflow

1. Identify the artifact class and agree on criteria before judging the design.
2. Check mechanical conditions: clipping, overflow, typography, contrast,
   geometry, assets, and palette. Measure source properties when available.
3. Resolve mechanical failures before evaluating composition and hierarchy,
   unless a broader diagnostic review is explicitly requested.
4. Compare rendered copy against approved source in both directions: missing
   content and unsupported additions both matter.
5. Calibrate criteria with known-good examples and deliberate defects. A test
   whose selector matches nothing must not silently pass.
6. Report each measured value against its threshold. Mark subjective findings
   as review judgments and unavailable checks as not checked.

## Output

An evidence-based report, blocked or unavailable checks, and concrete corrections.

## Adapt before use

Provide a measurement/rendering toolchain and artifact-specific rubric. Do not
infer exact type sizes from raster images or reuse another project's brand thresholds.
