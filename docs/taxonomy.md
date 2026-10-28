# Subjects, approaches, and disclosures

These are the implemented schema 1.0 values. The [canonical schema](https://synapse.ctrlchaos.io/synapse/schema) is authoritative. This guide explains them; it does not introduce new categories or change existing records.

## Subjects

Each record has one subject:

- Mathematics
- Engineering
- Computer science
- Physics and aerospace
- Economics and finance
- Philosophy
- Other

Choose the closest fit. Everyday life, history, arts, and other interests are welcome; use **Other** where no listed subject fits. Subject is a discovery aid, not a judgment about difficulty or the contributor’s identity. Do not silently rename stored values or add unsupported filter options.

## Tags

Tags are free-form topical labels, not a controlled list. Schema permits at most 12, each nonblank and at most 40 characters. Prefer clear, reusable spellings. Do not add private names or account identifiers, or infer education, occupation, expertise, or intelligence. These naming suggestions are editorial guidance rather than additional schema rules.

## Reasoning approaches

A record may have up to seven approach values describing what is visible in the exchange:

| Stored value | Use when the exchange includes |
| --- | --- |
| Testing assumptions | Examining a premise or trying a counterexample |
| Comparing alternatives | Considering different explanations or choices |
| Building a model | Constructing a simplified representation |
| Connecting ideas | Linking concepts or subjects |
| Revising a belief | An explicit revision visible in the messages |
| Tracing a mechanism | Asking how a process produces an outcome |
| Seeking evidence | Asking for observations, sources, or tests |

These descriptions guide selection; they do not claim access to hidden reasoning or prove that someone changed their complete beliefs.

## Purpose

The required purpose is one of **Understand**, **Solve**, **Decide**, or **Investigate**. It describes the selected exchange, not the person’s ability or occupation.

## Verification and provenance

Verification values are **Not checked**, **Partly checked by contributor**, and **Checked by contributor**. They report the contributor’s disclosure; they are not independent editorial fact-checking.

Provenance is **contributor_selected** or **illustrative**. Invented material must use `illustrative` and `is_illustrative: true`; contributor-selected material uses `is_illustrative: false`. Both fields must agree. Illustrative examples are not real community submissions or evidence that a provider generated the dialogue.

## Compatibility

Propose improvements through a public issue without disclosing unpublished conversations. Maintainers must review schema, website filters, existing records, and compatibility together before changing stored values. Category proposals are not already-implemented features.
