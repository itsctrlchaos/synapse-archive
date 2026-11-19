# Contributing to Synapse

An interesting question and a thoughtful follow-up are enough to start. Perfect English, specialist knowledge, a paid AI subscription, and a GitHub account are not required.

**[Share through the website](https://synapse.ctrlchaos.io/synapse/contribute). Do not put unreviewed transcripts in public issues or PRs.**

## Prepare the exchange

Choose a conversation, or a connected excerpt, from an AI tool you already use.

1. Keep the original human wording, speaker order, and enough AI replies to explain the follow-ups.
2. Include corrections, challenges, changed assumptions, or unresolved questions when they are part of the exchange.
3. Remove private or confidential information. Mark omissions as `[omitted]` and redactions as `[redacted]` where appropriate; disclose editing in the proposed record.
4. Do not fabricate missing exchanges, infer hidden model reasoning, or rewrite a participant to sound more knowledgeable.
5. Add optional context or your own short reflection if it helps someone understand why you selected the conversation.

A short exchange can be useful. Depth is not a score based on length, jargon, or expertise.

## Option A: import a public shared-chat link

On [Share your conversation](https://synapse.ctrlchaos.io/synapse/contribute), choose **Paste a public/shared-chat link**, enter the URL and select **Preview conversation**. Both sharing options are visible from the start.

Synapse automatically retrieves complete supported conversation text when the provider allows it. Read the actual preview, optionally edit or redact it, save changes, then confirm current publication permission and privacy before pressing **Publish**. No mandatory moderator approval or contributor GitHub account is required. No AI inference API call is needed.

Review everything the original link exposes, not just the excerpt you intend to publish. The original URL and unredacted baseline stay private by default. A URL alone is never republication permission. If attachments or interactive layouts are omitted, inspect the disclosure and explicitly accept the displayed text-only version. Unsupported or uncertain content must not be treated as a complete import.

### Supported shared links

| Provider | Accepted shape | Availability |
| --- | --- | --- |
| ChatGPT | `https://chatgpt.com/share/<share-id>` | Automatic supported text import, including a restricted anonymous browser reader for preview-only server HTML |
| Gemini | `https://gemini.google.com/share/<share-id>` | Automatic supported text import |
| Gemini short links | `https://g.co/gemini/share/<share-id>` or `https://share.gemini.google/<share-id>` | Only validated redirects to the supported Gemini share page |
| Claude | `https://claude.ai/share/<share-id>` | Accepted URL format; the verified server environment is blocked by the provider, so use copied-text recovery when it cannot be read |

ChatGPT/Claude IDs accept 36 hexadecimal/hyphen characters. Direct Gemini and g.co IDs accept 6–100 letters, digits, underscores or hyphens; share.gemini.google IDs accept 6–100 letters/digits. A trailing slash is accepted. Submitted links require HTTPS and exactly the host/path above, without credentials, explicit ports, fragments or query parameters. Accepted syntax does not establish availability, authenticity or affiliation.

Private, blocked, deleted, unavailable or incomplete shares remain private with a clear explanation. Synapse does not ask for a provider login or solve access challenges. It never invents missing messages. Retry a transient failure or use the recovery option below.

## Option B: paste or upload copied conversation text

Choose **Paste or upload conversation text** in the same flow. Copy selected messages with clear speaker labels and original code fences. Paste that copy, or save it as UTF-8 `.txt`/`.md` and upload it. The limit is 1 MB and 250,000 characters. PDFs, images, provider account exports and other file formats are not supported.

Use **Preview conversation**, check message boundaries, human/assistant labels, wording and order, and optionally edit/redact. If boundaries are ambiguous, correct standalone Human: and Assistant: labels; do not transcribe or fabricate exchanges. Editing does not require writing JSON or entering each message individually. A title and anonymous display name are supplied by default; changing them is optional.

Copied/uploaded text is contributor supplied, not independently verified against its source. Non-text material is excluded and requires explicit text-only acceptance. Read the entire preview, confirm the current terms and privacy, then press Publish. Any edit clears confirmation and requires review of the new exact version. Basic submission has no AI API dependency or email-submission route.

The current form does not contain the former preparation-prompt or prepared-JSON interface. If you use an AI preparation prompt elsewhere, it can use only messages in that chat or excerpts you provide, not your entire account history. Inspect its output and exclude preparation instructions from the actual exchange.

## Privacy and consent

Check for names and contact details, credentials and secret keys, confidential employer/client material, information about other people, and third-party material you cannot share. A nickname or Anonymous changes attribution only; the conversation itself may still identify you or someone else. There is no automated anonymization guarantee.

Before submission, read the [actual terms mvp-v1](https://synapse.ctrlchaos.io/synapse/guidelines#terms). The form explains public archive publication and commercial reuse before the unchecked permission confirmation. Permission covers only rights you own or are authorized to license in approved public content. [Licensing scope](RIGHTS.md).

Private originals, consent, review history, rejected submissions, moderator notes, references, and abuse-prevention data stay out of the public archive. MVP policy retains private workflow material without automatic deletion; Abe reviews deletion requests through the [private contact route](https://ctrlchaos.io/contact).

## Review and publication

A private preview is not public. Only after you confirm current terms and privacy and press Publish does the exact saved public version enter an archive branch/PR. Public branches and PRs are already visible before merge. The application checks and automatically merges only the matching confirmed PR, then refreshes the website. Pending checks and recoverable failures reuse the same job; use Retry publication status if automatic checking pauses. There is no routine GitHub visit or separate refresh click. Existing pending submissions are not automatically published. Publication success links to the public conversation, never a private draft URL.

For an unpublished withdrawal, contact the project privately with your submission reference. There is no self-service withdrawal button. For a public correction or removal, follow [reporting and removal](docs/reporting-and-removal.md); public history and external copies may remain.

## Documentation, public issues, and PRs

Public collaboration is appropriate for documentation fixes, safe reports about published records, broken links, and taxonomy proposals. Include a public record ID or URL when relevant, and keep sensitive evidence private. Do not include unpublished messages, private notes, consent, account details, or credentials in a branch, PR, issue, or attachment.

Maintainers should preserve record IDs/slugs, check public-field and provenance rules, and complete privacy and permission review before writing any conversation change to a public branch. Passing schema validation does not establish consent. Website source and private operational configuration are maintained separately.
