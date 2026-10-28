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

## Option A: paste conversation text

On [Share your conversation](https://synapse.ctrlchaos.io/synapse/contribute), choose **Paste conversation text**.

- Paste only the selected messages, then use **Separate messages for review**.
- Check message boundaries, human/assistant labels, and exact wording. Correct parser mistakes yourself.
- Supply a title and subject. Review optional metadata, disclosure, public display name, and your own reflection. You can use a nickname or Anonymous.
- Use **Preview public contribution** and read the entire proposed public record.
- Read the contribution terms, including commercial reuse for rights you can grant, then explicitly confirm permission and submit for private review.

Your selected original and proposed public version enter a private queue. A success reference is a private submission reference, not a publication URL. No contact email is collected by this form.

## Option B: submit a shared-chat link

Choose **Paste a public/shared-chat link**. You do not need to paste a transcript first.

Review **everything the link exposes**, not just the messages you hope to publish. Check privacy, permission, and third-party text before confirming the terms and submitting the link.

The URL is saved privately **awaiting manual import and review**. Automatic importing is unavailable. A moderator must obtain and import actual messages, check them, and approve the public version. Saving the URL is not “conversation imported.” A public link alone is not republication permission.

Links can expire, be revoked, or require sign-in. Use pasted text if a link is unavailable or unsuitable. Synapse makes no AI API call for basic text or link intake and offers no email-submission route.

### Supported shared links

| Provider | Accepted shape | Share ID rule |
| --- | --- | --- |
| ChatGPT | `https://chatgpt.com/share/<share-id>` | 36 characters made of hexadecimal digits and hyphens |
| Claude | `https://claude.ai/share/<share-id>` | 36 characters made of hexadecimal digits and hyphens |
| Gemini | `https://gemini.google.com/share/<share-id>` | 6 to 100 letters, digits, underscores, or hyphens |

A trailing slash is accepted. Use HTTPS with exactly the host shown; credentials, explicit ports, fragments, and query parameters are rejected. The ChatGPT/Claude rule accepts hexadecimal letter case; do not infer from syntax validation that the link is available or genuinely public. For other providers, paste the selected text.

These are implemented intake formats, not a claim of affiliation with the providers.

## Optional preparation prompts

Under **Paste conversation text**, expand **Optional help: prepare a conversation with AI** on the [contribution page](https://synapse.ctrlchaos.io/synapse/contribute). It offers prompts for preparing a selected exchange, finding connected questions, or capturing a moment understanding changed. **Advanced: import a prepared JSON conversation** is optional; ordinary text remains sufficient.

A prompt can work only with messages actually available in the current chat or excerpts you provide. It cannot retrieve your entire account history. Inspect the result message by message, preserve original wording, and exclude preparation instructions and their output from the exchange. Write your own reflection. Prompts do not guarantee privacy, accuracy, or suitability.

## Privacy and consent

Check for names and contact details, credentials and secret keys, confidential employer/client material, information about other people, and third-party material you cannot share. A nickname or Anonymous changes attribution only; the conversation itself may still identify you or someone else. There is no automated anonymization guarantee.

Before submission, read the [actual terms mvp-v1](https://synapse.ctrlchaos.io/synapse/guidelines#terms). The form explains public archive publication and commercial reuse before the unchecked permission confirmation. Permission covers only rights you own or are authorized to license in approved public content. [Licensing scope](RIGHTS.md).

Private originals, consent, review history, rejected submissions, moderator notes, references, and abuse-prevention data stay out of the public archive. MVP policy retains private workflow material without automatic deletion; Abe reviews deletion requests through the [private contact route](https://ctrlchaos.io/contact).

## Review and publication

Private submission, private approval, a public PR, manual merge, and website refresh are distinct steps. Only the approved public version may be placed in a public branch or PR. Public branches and PRs are already visible before merge. A maintainer manually merges, then refreshes the website from the archive. Submission does not guarantee acceptance or immediate publication.

For an unpublished withdrawal, contact the project privately with your submission reference. There is no self-service withdrawal button. For a public correction or removal, follow [reporting and removal](docs/reporting-and-removal.md); public history and external copies may remain.

## Documentation, public issues, and PRs

Public collaboration is appropriate for documentation fixes, safe reports about published records, broken links, and taxonomy proposals. Include a public record ID or URL when relevant, and keep sensitive evidence private. Do not include unpublished messages, private notes, consent, account details, or credentials in a branch, PR, issue, or attachment.

Maintainers should preserve record IDs/slugs, check public-field and provenance rules, and complete privacy and permission review before writing any conversation change to a public branch. Passing schema validation does not establish consent. Website source and private operational configuration are maintained separately.
