# From private submission to public discovery

Synapse is the community project and website. This repository is its canonical collection of published records. The application source and private review system are maintained separately and are not distributed here.

## The publication boundary

| Stage | Visibility and meaning |
| --- | --- |
| Selected text or shared link is submitted | Private queue; no public record is created |
| Moderator imports a link, if needed, and reviews | Original material, permission, proposed public version, and editing/privacy decisions stay private |
| Exact public version is approved | Still a private approval, not publication |
| Approved content enters an archive branch and PR | Already public; nothing unreviewed or private may be included |
| Maintainer manually merges into main | Canonical published archive content |
| Website successfully refreshes from main | The validated snapshot becomes available to public browsing and search |

Only reviewed public fields cross this boundary. Private originals, consent, moderator notes, review history, authentication, abuse counters, and publication-job state do not belong in the archive. An open PR, private database state, or submission receipt is not proof of publication.

Shared links are stored without automatic fetching or importing. Actual messages must be imported manually before approval. Basic submission does not need an AI inference API or contributor GitHub account. [Contribution options](../CONTRIBUTING.md).

## Website refresh and search

A maintainer uses **Refresh archive snapshot** after an archive addition, correction, or removal. The publication interface also offers **Check merge and refresh website**. There is no automatic archive webhook or scheduled refresh in this MVP. A documentation PR does not itself refresh or deploy the private website.

The refresh reads a single resolved default-branch commit and validates the collection, including filenames, IDs, slugs, publication dates, provenance, and message references. Only a complete valid snapshot replaces the prior public snapshot. Failed, incomplete, or invalid refreshes retain the last-known-good public content. A confirmed empty collection is a valid state after removal.

After successful refresh, a short process cache can delay visibility by about 30 seconds. If no successful refresh has occurred, older content can remain visible longer. Do not promise instant publication or removal.

The website’s public snapshot is separate from private submissions. Public reading does not depend on the private queue being available. Its search index is rebuilt from validated public records; it is not another canonical archive. Search covers titles, context, messages, reflections, and tags, with the existing metadata filters.

## Scope of this repository

This repository distributes public JSON, documentation, and the header artwork. No deployment workflow, package, private service configuration, or analysis tool is supplied here. The website may display additional built-in illustrative examples outside the archive; those do not establish community activity or the contents of this repository.

## Changes and recovery

Correct or remove public records through a reviewed archive change and manual merge, then refresh the website. Preserve stable IDs and slugs for corrections. A private rejection or withdrawal flag does not remove an already-public record. [Reporting and removal](reporting-and-removal.md) describes the reader-facing process and limits.

Canonical records can rebuild the public snapshot and derived search index. Public history, forks, clones, and downloaded copies can retain older versions even after the current file is removed.
