# From private preview to public discovery

Synapse is the website and community project. This repository is its canonical published collection. Website source and private workflow data are maintained separately.

## The publication boundary

| Stage | Visibility and meaning |
| --- | --- |
| Import a readable public link or supply selected text | Private browser-authorized draft; no public record |
| Contributor reads, optionally edits/redacts and saves | Original, draft, permission state and private notes stay private |
| Contributor confirms current terms/privacy and presses Publish | Exact saved version is frozen for publication; moderator approval is optional |
| Matching archive branch and PR are created | Already public; only confirmed public fields cross the boundary |
| Repository checks permit the exact PR to merge automatically | Canonical record on main; protections are not bypassed |
| Validated archive refresh completes and bounded warm readers expire | Public detail, browsing/search and JSON export reflect the current archive |

Private originals, consent, notes, history, authentication and publication-job metadata never belong here. A saved URL, open PR or private job status alone is not proof of publication. Existing pending submissions and old consent do not authorize new automatic publication.

## Import and recovery

ChatGPT and Gemini import complete supported text when retrieval succeeds. ChatGPT can use a restricted anonymous browser transport for preview-only server HTML. Claude is blocked in the verified server environment and requires copied-text recovery when inaccessible. Deleted, private, incomplete or unsupported shares remain private. Attachment/layout omissions must be disclosed and accepted; missing exchanges are never invented. Pasted/UTF-8 .txt/.md recovery is contributor supplied, not independently source verified. Basic submission needs no AI inference API, contributor account or GitHub login. [Contribution guide](../CONTRIBUTING.md).

## Refresh, search and removal

The existing publication job automatically checks the exact matching PR, merges when checks permit, and refreshes from the archive. Bounded browser polling can be resumed using the same job; it does not require a new publication or a website rebuild. Owner controls can pause intake/publication and remove content through a matching removal PR and refresh. Manual corrections made outside the application require a successful archive refresh. Documentation changes alone do not deploy the website or refresh conversation data.

Refresh resolves main and validates filenames, IDs, slugs, dates, provenance, message references and capacity before atomically replacing the public snapshot. Invalid or interrupted refreshes do not overwrite it. A confirmed empty archive is valid. Warm readers retain their last successful snapshot for at most 30 seconds; if storage is unavailable beyond that bound, reading fails rather than indefinitely serving removed content. Completion waits for the bounded warm-reader interval and a shared-snapshot recheck. This is not a claim that every browser or external copy was observed or erased.

Public reading/search/export do not read the private submission database. The search index is rebuilt from validated public records and is not another canonical archive. Published records here can rebuild the snapshot and index. [Corrections and removal](reporting-and-removal.md).

## Repository scope

This repository distributes published JSON, documentation and project artwork. It contains no private service configuration, website source, deployment workflow or analysis service. Built-in website illustrations may exist outside the archive and do not establish community activity. Git history, forks, clones and downloaded copies can retain earlier versions after current content is removed.
