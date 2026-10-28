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

A maintainer reviews the concern and prepares a correction or removal in the public archive. Corrections preserve stable IDs/slugs and disclose substantive changes or redactions. Only content safe for public release may enter a public branch or PR, and the maintainer manually reviews/merges the change.

After merge, the website must successfully refresh its validated snapshot from the archive. Only then does the new version appear, or the removed record leave public search, the reader, and public JSON export. Private moderation flags do not remove public content.

No automatic archive webhook or scheduled refresh is present in the MVP. A failed or unrequested refresh can leave the last-known-good snapshot visible; the maintainer must retry. A short process cache can add about 30 seconds after a successful refresh. There is no separate urgent suppression tool or promised removal deadline.

## Limits of removal

Removing the current file cannot guarantee erasure from Git history, earlier PRs, forks, clones, downloads, caches, or third-party copies. Removal from Synapse does not revoke CC BY 4.0 permissions already granted while its conditions are followed. Separate third-party and privacy rights still apply. [Rights and licensing scope](../RIGHTS.md).
