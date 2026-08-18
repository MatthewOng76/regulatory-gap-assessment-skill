# Regulatory Gap Assessment Skill

A reusable, model-agnostic skill for rigorous regulatory gap analysis in Excel.

## What it does

This skill is designed for line-by-line, section-by-section regulatory gap analysis where:
- every atomic regulatory requirement is preserved verbatim before interpretation
- internal evidence is assessed iteratively and cumulatively
- reassessments do not overwrite prior rows
- outputs remain usable in Excel for sorting, filtering, and pivot analysis

## Core idea

Change the capsule. Keep the machine.

The model provides inference.
The methodology, structure, guardrails, and workflow live outside the model.

That means the same capability can work with frontier models, private deployments, or capable local models without rebuilding the workflow itself.

## Contents

- `skill/regulatory-gap-assessment.md` — the skill/spec file
- `docs/index.html` — public landing page for the skill

## Public page

Intended for GitHub Pages.

## Positioning

This is a practical example of model-agnostic workflow design applied to:
- regulatory gap analysis
- cumulative multi-document evidence assessment
- append-only reassessment history
- Excel-native auditability
