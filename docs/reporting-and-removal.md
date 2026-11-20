# Reporting, corrections, withdrawal, and removal

Start with [Report or request removal](https://synapse.ctrlchaos.io/synapse/report).

## Choose a safe channel

| Concern | Where to report it |
| --- | --- |
| Broken link, formatting error, or safe correction to a published record | [Public archive issue](https://github.com/itsctrlchaos/synapse-archive/issues), identifying the public record ID/URL |
| Unpublished submission, privacy or rights concern, or sensitive evidence | [Private project contact](https://ctrlchaos.io/contact), with the record ID or private submission reference and only necessary details |

GitHub issues, PRs, branches, and attachments are public. Do not post unpublished transcripts, consent records, contact information, credentials, identity documents, or other sensitive evidence there. If public issues are unavailable, use the private contact route. The website form is the conversation-submission entry point; contact is for project concerns, not an email-submission feature.

## Unpublished material

There is no self-service withdrawal control in the MVP. Ask the maintainer privately to withdraw an unpublished submission or review a deletion request, quoting your submission reference if available. Do not create a public issue containing that reference or transcript.

Current MVP policy retains originals, rejected submissions, permission records, and review history without automatic deletion. Abe reviews requests. A request does not imply an automatic deletion operation or a guaranteed response deadline.

## Published records

The owner reviews the concern. An authenticated owner removal creates the matching removal PR, automatically merges when repository checks permit, and refreshes the website. Corrections require a reviewed archive update, preserving stable IDs/slugs and disclosing substantive changes or redactions. Only content safe for public release may enter a public branch or PR.

After merge, the website must successfully refresh its validated snapshot from the archive. Only then does the new version appear, or the removed record leave public search, the reader, and public JSON export. Private moderation flags do not remove public content.

The application removal job automatically refreshes and reconciles the website. Pending checks or a cache outage remain pending and can be resumed safely. Warm readers have a maximum 30-second lifetime; after that, unavailable shared storage causes a read failure rather than indefinite stale serving. A manual correction outside the application still needs a successful refresh. There is no promised removal deadline or internet-wide erasure guarantee.

## Limits of removal

Removing the current file cannot guarantee erasure from Git history, earlier PRs, forks, clones, downloads, caches, or third-party copies. Removal from Synapse does not revoke CC BY 4.0 permissions already granted while its conditions are followed. Separate third-party and privacy rights still apply. [Rights and licensing scope](../RIGHTS.md).
