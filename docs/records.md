# Public record format

Published conversations are UTF-8 JSON files in `explorations/<id>.json`. The stable UUID identifies a record; its slug provides the website URL. Schema version **1.0** is implemented by the website and available as [canonical generated JSON Schema](https://synapse.ctrlchaos.io/synapse/schema). This reference explains that schema rather than defining a second one.

## Fields

All top-level fields are required. Optional information uses the permitted empty string, empty array, or `null`, rather than omitting a field. Objects reject unknown properties. Character limits below follow JavaScript string length.

| Field | Shape and machine-validated limits |
| --- | --- |
| `schema_version` | Exactly `"1.0"` |
| `id` | UUID; must match the JSON filename on archive ingestion |
| `slug` | Lowercase letters and digits separated by single hyphens; at most 160 characters |
| `title` | Nonblank string, at most 160 characters |
| `context` | String, at most 4,000 characters; may be empty |
| `subject` | One [subject value](taxonomy.md#subjects) |
| `tags` | Up to 12 nonblank strings, each at most 40 characters |
| `reasoning_approaches` | Up to seven [approach values](taxonomy.md#reasoning-approaches); may be empty |
| `purpose` | One of `Understand`, `Solve`, `Decide`, `Investigate` |
| `contributor_display_name` | Nonblank string, at most 80 characters; `Anonymous` is supported |
| `ai_provider` | Nonblank string, at most 80 characters; `Unknown` when not supplied |
| `ai_model` | Nonblank string, at most 100 characters; `Unknown` when not supplied |
| `language` | Nonblank string, at most 80 characters; `Unknown` when not supplied |
| `conversation_date` | ISO calendar date (`YYYY-MM-DD`) or `null` when unknown |
| `published_at` | ISO UTC datetime, such as `2026-10-27T19:34:00.000Z`; published records require a non-null value |
| `messages` | 1 to 400 ordered message objects; see below |
| `annotations` | Up to 100 objects with `message_id` (string up to 80 characters) and `text` (nonblank, up to 2,000 characters); references must identify existing messages |
| `reflection` | String up to 6,000 characters; may be empty |
| `unresolved_questions` | Up to 30 nonblank strings, each up to 1,000 characters |
| `source_url` | Public HTTPS URL without username or password, up to 2,000 characters, or `null` |
| `verification_status` | `Not checked`, `Partly checked by contributor`, or `Checked by contributor` |
| `editing_disclosure` | String up to 4,000 characters; may be empty in the schema |
| `provenance_type` | `contributor_selected` or `illustrative` |
| `is_illustrative` | Boolean; true exactly when provenance is `illustrative` |

Each message has exactly three fields:

| Field | Rule |
| --- | --- |
| `id` | 1 to 80 ASCII letters, digits, or hyphens; unique within the record |
| `role` | `human` or `assistant` |
| `text` | Nonblank string up to 100,000 characters; original visible wording |

Array order preserves the conversation sequence. Total message text cannot exceed 200,000 characters. The collection validator also rejects duplicate record IDs and slugs. There are no per-message timestamps, private contact fields, consent records, or hidden-reasoning fields in this public format.

The record's `source_url` rule is broader than the [supported shared-link intake formats](../CONTRIBUTING.md#supported-shared-links). A valid source URL is stored as metadata; schema acceptance does not establish availability, authenticity, ownership, or permission.

## Validation and editorial review

The generated JSON Schema describes field shapes. Application validation additionally checks message-ID uniqueness, annotation targets, consistent illustrative disclosures, total transcript length, non-null publication dates, collection uniqueness, and archive filenames. Reading only the JSON Schema is not a replacement for these checks.

Privacy, consent, rights, truthful editing disclosures, suitable taxonomy, and preserving meaning are editorial requirements. Passing a machine validator does not make content safe or approved for publication. `verification_status` is contributor-reported, not independent fact-checking. Do not infer provider authenticity or personal beliefs from metadata.

An illustrative record must identify itself as such. Unknown dates use `null`; missing provider/model/language information uses `Unknown` in the contribution flow. The scripted example below uses explicit not-applicable labels because it does not represent a real provider session.

## Complete approved example

This is the existing [published synthetic cache example](../explorations/8a74bc63-8571-4cc3-9bee-31fb0404c9cb.json), reproduced in full for reference. It is not a new archive entry or a real contributor exchange. The file in `explorations/` remains canonical.

```json
{
  "schema_version": "1.0",
  "id": "8a74bc63-8571-4cc3-9bee-31fb0404c9cb",
  "slug": "synthetic-example-why-a-cache-needs-a-size-limit",
  "title": "Synthetic example: why a cache needs a size limit",
  "context": "A newly scripted illustration for testing Synapse publication. This is not a real contributor conversation and contains no private submission material.",
  "subject": "Computer science",
  "tags": [
    "caching",
    "memory limits",
    "synthetic example"
  ],
  "reasoning_approaches": [
    "Tracing a mechanism"
  ],
  "purpose": "Understand",
  "contributor_display_name": "Synapse synthetic example",
  "ai_provider": "Not applicable (scripted example)",
  "ai_model": "Not applicable",
  "language": "English",
  "conversation_date": null,
  "published_at": "2026-10-27T19:34:00.000Z",
  "messages": [
    {
      "id": "m1",
      "role": "human",
      "text": "If a cache makes lookups faster, why not let it keep everything?"
    },
    {
      "id": "m2",
      "role": "assistant",
      "text": "A cache uses limited memory. Without a size limit, keeping more entries can consume memory needed by the rest of the application."
    },
    {
      "id": "m3",
      "role": "human",
      "text": "So reaching the limit should remove something, rather than refuse every new item?"
    },
    {
      "id": "m4",
      "role": "assistant",
      "text": "That is one common choice. A least recently used policy removes the entry that has gone unused for the longest time, making room for a new entry. The best policy depends on the workload."
    }
  ],
  "annotations": [],
  "reflection": "Synthetic example: a follow-up connects a performance benefit to a resource limit. No real person's thinking or experience is represented.",
  "unresolved_questions": [
    "Which eviction policy fits a workload with frequently repeated lookups?"
  ],
  "source_url": null,
  "verification_status": "Not checked",
  "editing_disclosure": "Entire dialogue and reflection scripted for a publication test; no original conversation was imported, paraphrased, or redacted. For rights the contributor can grant, this example is offered under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/), including commercial reuse with attribution. This does not license any rights the contributor does not own or control.",
  "provenance_type": "illustrative",
  "is_illustrative": true
}
```
