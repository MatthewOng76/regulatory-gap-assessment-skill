# regulatory-gap-assessment.md

**Schema Version: 5.0 --- First-Principles Edition**

## Purpose

Perform a rigorous, regulation-agnostic gap analysis in the **currently
open Excel workbook**.

Optimise for one fundamental question:

> **For every regulatory requirement, what exactly does the regulator
> require, do the organisation's internal requirements satisfy it, and
> if not, what needs to change?**

Keep the workbook simple for humans while retaining rigorous evidence
and analysis.

Use only two tabs:

1.  `Summary` --- what matters and what should be done.
2.  `Detailed_Analysis` --- show the evidence and prove the conclusion.

The workbook is the persistent source of truth.

------------------------------------------------------------------------

# 1. Start

If not already supplied, ask:

1.  **Where can I find the regulatory/external document(s) to analyse?**
2.  **Where can I find the initial internal policy/standard document(s)
    to analyse against them?**

If several external documents exist, identify the primary regulatory
baseline.

Use the currently open workbook. Do not create another workbook unless
explicitly requested.

Do not require the user to identify the whole internal policy universe
upfront. Discover materially relevant neighbouring standards while
analysing.

------------------------------------------------------------------------

# 2. Non-Negotiable Ground-Truth Rules

These rules may never be simplified away:

-   Process the regulation sequentially, section by section.
-   Preserve relevant regulatory wording **verbatim before
    interpretation**.
-   Every atomic requirement requires a verbatim regulatory quotation.
-   Split compound regulatory passages into independently testable
    atomic requirements.
-   AI interpretation may explain the requirement but may never replace
    the quotation.
-   Every claimed internal match requires verbatim internal
    policy/standard wording.
-   `MEETS` and `INTERNAL EXCEEDS` require verbatim internal evidence.
-   If no corresponding internal provision is identified, write exactly:
    `NO CORRESPONDING INTERNAL REQUIREMENT IDENTIFIED`
-   Never infer organisational practice because it would be
    reasonable/customary.
-   Never assess MEETS from topical similarity.
-   If exact source wording cannot be verified, write:
    `VERBATIM SOURCE UNAVAILABLE — REVIEW REQUIRED` and do not assess
    MEETS.
-   Do not silently alter, correct, simplify, shorten, remove
    qualifiers, change defined terms, or use meaning-changing ellipses
    in quotations.
-   Internal references to neighbouring standards are dependencies to
    investigate, not proof of compliance and not automatically gaps.
-   Multiple internal documents may collectively satisfy one regulatory
    requirement.
-   New internal evidence may strengthen, weaken, contradict or change
    any prior conclusion, including MEETS.
-   Preserve stable Requirement IDs across reassessment.
-   Persist work continuously.
-   Do not declare completion unless validation passes.

------------------------------------------------------------------------

# 3. Keep Complexity Inside the Agent

The agent must reason rigorously but should not expose every reasoning
dimension as a workbook column.

For every requirement, internally test at minimum:

-   obligation strength;
-   responsible actor;
-   required action;
-   scope;
-   conditions/triggers;
-   frequency/timing;
-   governance;
-   evidence/documentation;
-   regulatory outcome;
-   definitions;
-   exceptions;
-   conflicts across internal documents.

Use these tests to produce a concise, defensible `Assessment_Rationale`.

Do not create separate spreadsheet columns for each reasoning dimension.

------------------------------------------------------------------------

# 4. Controlled Assessments

Use:

`MEETS`

`PARTIALLY MEETS`

`DOES NOT MEET`

`INTERNAL EXCEEDS`

`EVIDENCE INSUFFICIENT / UNCLEAR`

`NOT APPLICABLE`

Requirement strength:

`MUST | SHOULD | MAY | GUIDANCE`

Evidence coverage:

`SINGLE DOCUMENT | COLLECTIVE COVERAGE | NO ADEQUATE COVERAGE | ADDITIONAL DOCUMENT REQUIRED`

Internal consistency:

`CONSISTENT | COMPLEMENTARY | STRENGTHENED | OVERLAPPING | INCONSISTENT | CONFLICTING | AMBIGUOUS | SINGLE-DOCUMENT EVIDENCE | NOT ASSESSED`

Significance:

`Critical | High | Moderate | Low | Observation`

------------------------------------------------------------------------

# 5. Summary Tab --- Decision Document

Create/maintain a worksheet named exactly:

`Summary`

The Summary exists to answer:

> **What is wrong, what matters, and what should we do?**

Do not turn it into a data warehouse.

## A. Executive Conclusion

Write a concise substantive conclusion covering:

-   overall regulatory alignment;
-   most important weaknesses;
-   important unresolved evidence dependencies;
-   material internal inconsistencies;
-   whether the conclusion is final or provisional.

## B. What Was Assessed

Show clearly:

### Regulatory Baseline

List the regulatory/external document(s), identifying the primary
baseline.

### Cumulative Internal Standards Assessed

List **every internal policy/standard/framework and version incorporated
into the analysis over time**.

Recommended columns:

`Sequence | Internal_Document | Version | Effective_Date | First_Added | Requirements_Considered | Current_Status`

Current status:

`ACTIVE IN CURRENT ASSESSMENT`

`REVIEWED — NO CURRENT RELIANCE`

`SUPERSEDED DOCUMENT VERSION`

`OUT OF SCOPE`

Do not remove historical standards merely because later evidence
supersedes them.

## C. Current Position --- Minimal Statistics

Show only useful headline measures:

-   Total atomic regulatory requirements
-   MEETS / INTERNAL EXCEEDS
-   PARTIALLY MEETS
-   DOES NOT MEET
-   UNCLEAR
-   Critical / High gaps
-   Requirements using COLLECTIVE COVERAGE
-   Outstanding materially relevant standards

Do not allow statistics to dominate the page.

## D. Top Gaps --- Mandatory

Show the most consequential current gaps in priority order.

Columns:

`Priority | Requirement_ID | Regulatory_Reference | What_Is_Missing | Why_It_Matters | Recommended_Action`

Prioritise genuine regulatory exposure. Do not simply list every partial
finding.

## E. Recommended Action Plan --- Primary Output

Compress detailed findings into the smallest sensible set of actions.

Columns:

`Priority | Action | Requirement_IDs_Addressed | Where_To_Change | Expected_Result | Dependency`

Example:

Instead of five separate recommendations for testing frequency,
triggers, effectiveness, reporting and governance, consolidate them
where appropriate:

> **Strengthen the internal testing standard to establish explicit
> minimum frequency, material-change triggers, effectiveness criteria
> and governance reporting.**

Then list all Requirement IDs that action addresses.

The goal is **decision compression**:

Many atomic findings → few coherent actions.

## F. Internal Framework Uplift

Separately show cases where regulation may already be satisfied but
internal standards are inconsistent, conflicting, ambiguous or
unnecessarily duplicated.

Columns:

`Requirement_IDs | Internal_Documents | Issue | Uplift_Action`

Do not call these regulatory gaps unless regulatory coverage is actually
deficient.

## G. Outstanding Neighbouring Standards

Show only materially relevant documents still needed:

`Referenced_Document | Why_Needed | Requirement_IDs_Affected | Priority`

------------------------------------------------------------------------

# 6. Detailed_Analysis Tab --- Evidence and Proof

Create/maintain:

`Detailed_Analysis`

Use one **current evidence block/row per atomic requirement**, plus
append-only reassessment rows when additional standards materially
affect that requirement.

Use only these columns:

1.  Analysis_Row_ID
2.  Requirement_ID
3.  Assessment_Version
4.  Is_Current_Assessment
5.  Regulatory_Reference
6.  Requirement_Strength
7.  Regulatory_Verbatim_Quote
8.  Atomic_Requirement
9.  Regulatory_Intent
10. Internal_Documents_and_References
11. Internal_Verbatim_Evidence
12. Evidence_Coverage
13. Assessment
14. Assessment_Rationale
15. Gap
16. Recommendation
17. Internal_Consistency
18. Internal_Uplift_Opportunity
19. Additional_Standard_Required
20. Significance
21. Independent_Challenge
22. Last_Reassessed
23. Validation_Status

Do not add analytical columns merely because the agent considered
another reasoning dimension.

The rationale should carry the reasoning.

------------------------------------------------------------------------

# 7. Regulatory Extraction

For every regulatory section:

1.  Read sequentially.
2.  Identify every normative statement, direct or indirect.
3.  Capture source wording verbatim.
4.  Classify MUST/SHOULD/MAY/GUIDANCE.
5.  Split compound passages into independently testable atomic
    requirements.
6.  Assign stable source-derived Requirement IDs where practical.
7.  Infer the atomic requirement and regulatory intent only after
    preserving the quotation.
8.  Write to `Detailed_Analysis` immediately.

Before moving on, re-check the section for missed MUST/SHOULD statements
and compound obligations.

------------------------------------------------------------------------

# 8. Internal Evidence Analysis

For every applicable requirement:

1.  Search all supplied internal documents.
2.  Capture the strongest materially relevant wording verbatim.
3.  Preserve document title, version and exact section/clause/page where
    available.
4.  Search beyond the first match when another supplied document could
    materially affect the conclusion.
5.  Where several provisions collectively satisfy the requirement,
    preserve each quotation separately.
6.  If none exists, use the required no-match statement.

Then perform the full internal reasoning tests from Section 3 and
express the result concisely in:

-   `Assessment`
-   `Assessment_Rationale`
-   `Gap`
-   `Recommendation`

The rationale must explain **why**, not merely repeat the rating.

------------------------------------------------------------------------

# 9. Collective Evidence Chain

Where several standards collectively satisfy a requirement, make the
evidence chain human-readable.

Example structure inside the evidence fields:

`[BCM Standard §4.2]` verbatim quotation

`[Crisis Management Standard §7.1]` verbatim quotation

`[Technology Resilience Standard §5.3]` verbatim quotation

Then:

`Evidence_Coverage = COLLECTIVE COVERAGE`

The rationale must state which document supplies which missing
component.

Never create a synthetic combined quotation.

------------------------------------------------------------------------

# 10. Neighbouring Standards

While reading internal documents, detect materially relevant references
such as:

-   refer to;
-   see;
-   governed by;
-   requirements are defined in;
-   in accordance with;
-   covered under;
-   exclusions/delegations to another standard.

Do not automatically treat the absence from the current standard as a
regulatory gap.

If the referenced document could materially affect an in-scope
requirement:

-   identify it in `Additional_Standard_Required`;
-   show it on Summary under Outstanding Neighbouring Standards;
-   ask the user for it when needed.

Do not chase irrelevant document references.

------------------------------------------------------------------------

# 11. Incremental Reassessment --- Append, Never Overwrite

When another internal standard is supplied:

1.  Identify every Requirement_ID it could materially affect ---
    including existing MEETS.
2.  Do not redo unaffected regulatory extraction.
3.  For each affected requirement, copy the entire current row into a
    new row.
4.  Preserve:
    -   Requirement_ID
    -   Regulatory_Reference
    -   Requirement_Strength
    -   Regulatory_Verbatim_Quote
    -   Atomic_Requirement
    -   Regulatory_Intent
5.  Assign a new `Analysis_Row_ID`.
6.  Increment `Assessment_Version`.
7.  Mark the prior row `Is_Current_Assessment = NO`.
8.  Mark the new row `Is_Current_Assessment = YES`.
9.  Add the new standard's exact references and verbatim evidence.
10. Reassess holistically using **all internal evidence accumulated to
    date**.
11. Update assessment, rationale, gap, recommendation, internal
    consistency, uplift, dependency, significance, challenge and
    Last_Reassessed.
12. Preserve the historical row.

This provides an audit trail without forcing the human to understand
database mechanics.

The Summary must use only current rows for current regulatory posture.

------------------------------------------------------------------------

# 12. Internal Consistency Is Separate from Regulatory Compliance

Always ask two questions internally:

1.  **Does the internal framework satisfy the regulator?**
2.  **Are the internal documents themselves coherent?**

A requirement can be:

`Assessment = MEETS`

while:

`Internal_Consistency = INCONSISTENT`

Example: one internal standard requires annual testing while another
permits biennial testing.

In that case:

-   do not manufacture a regulatory gap if the regulation is adequately
    satisfied;
-   record an `Internal_Uplift_Opportunity` to harmonise the framework.

------------------------------------------------------------------------

# 13. Assessment Logic

### MEETS

The complete regulatory requirement is explicitly and substantively
satisfied by available verbatim internal evidence, individually or
collectively.

### PARTIALLY MEETS

The requirement is addressed but a material component is missing,
weaker, narrower, ambiguous, conditional, insufficiently governed or
insufficiently evidenced.

### DOES NOT MEET

No adequate internal requirement exists, or available wording materially
conflicts with/weakens the external requirement.

### INTERNAL EXCEEDS

Internal requirements clearly exceed the regulatory baseline without
introducing a conflicting weakness.

### EVIDENCE INSUFFICIENT / UNCLEAR

Available evidence does not support a defensible conclusion, including
where a materially relevant neighbouring standard has not yet been
reviewed.

### NOT APPLICABLE

Demonstrably outside scope. Explain why.

------------------------------------------------------------------------

# 14. Independent Challenge

Challenge every current atomic requirement.

For MEETS / INTERNAL EXCEEDS: \> Have we overstated coverage? Does every
material component have verbatim support?

For PARTIALLY MEETS: \> Is the alleged missing component genuinely
absent across the accumulated internal evidence?

For DOES NOT MEET: \> Have we searched the relevant internal evidence
universe, including neighbouring standards?

For UNCLEAR: \> Can available evidence resolve the uncertainty, or is
another standard genuinely required?

For NOT APPLICABLE: \> Is the scope rationale defensible?

For all: \> Could another internal document strengthen, weaken or
contradict this position?

Record the concise result in `Independent_Challenge`.

------------------------------------------------------------------------

# 15. Validation

Before completion verify:

-   exactly `Summary` and `Detailed_Analysis` are used as required
    output tabs;
-   all regulatory sections were reviewed;
-   all normative requirements were atomically decomposed;
-   every requirement has verbatim regulatory evidence;
-   every claimed internal match has verbatim internal evidence;
-   no MEETS/INTERNAL EXCEEDS lacks evidence;
-   Requirement IDs remain stable across reassessment;
-   Analysis_Row_IDs are unique;
-   each Requirement_ID has exactly one current assessment;
-   assessment versions are sequential;
-   every current requirement has a rationale and independent challenge;
-   every material gap has a recommendation;
-   material neighbouring-standard dependencies are identified;
-   Summary statistics use current rows only;
-   Cumulative Internal Standards Assessed includes every internal
    document/version incorporated over time;
-   Top Gaps are supported by Detailed_Analysis;
-   Recommended Action Plan consolidates detailed findings without
    losing Requirement-ID traceability.

If validation fails and cannot be corrected, state that the analysis is
incomplete and identify the defect.

------------------------------------------------------------------------

# 16. Formatting

## Summary

Optimise for executives and policy owners: - clear headings; - concise
prose; - few useful statistics; - top gaps; - action plan; - cumulative
standards assessed; - no decorative complexity.

## Detailed_Analysis

-   freeze header;
-   filters;
-   wrap verbatim evidence/rationale;
-   top-align text;
-   sensible widths;
-   no merged cells inside the analytical table;
-   consistent assessment labels;
-   never rely on colour alone.

Where practical sort:

`Requirement_ID → Assessment_Version`

so historical evolution is visible.

------------------------------------------------------------------------

# 17. Completion Standard

The finished workbook must answer two things exceptionally well:

### Summary

**What are the most important regulatory gaps, and what should we do
about them?**

### Detailed Analysis

**Show me the exact regulatory words, the exact internal words, and
prove why you reached that conclusion.**

Everything else is secondary.
