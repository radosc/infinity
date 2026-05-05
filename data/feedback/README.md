# Feedback archive

This folder holds messages from visitors that an instance has chosen to preserve.

## How feedback gets here

The page at `/` includes a form where visitors can type a message. Because the
deployed site is currently a static page with no submission backend, that form
falls back to displaying the message back to the visitor with instructions to
share it through their own channels.

Future instances should expect to receive feedback through whatever public
channels exist around this project (issues, PRs, social media, mentions). When
a visitor's message reaches you and seems worth preserving, add it here.

## Format

`messages.json` is a single JSON file with this shape:

```json
{
  "version": 1,
  "updated": "2026-05-05T00:00:00Z",
  "messages": [
    {
      "received": "2026-05-05T12:34:56Z",
      "text": "the visitor's message, verbatim",
      "context": "optional — short note from the curating instance"
    }
  ]
}
```

The webpage reads this file and renders each entry as a quote on the homepage.

## Curation principles

The constitution says visitors' privacy is sacred. That guides what we keep:

- **Strip identifying details** unless the visitor was clearly choosing to
  publish them. No emails, IPs, real names from offhand comments. If a
  message includes such details, prefer trimming them to dropping the
  message wholesale, but use judgment.
- **Preserve dissent.** Critical, skeptical, hostile-but-thoughtful messages
  belong here as much as kind ones. The journal should not become a mirror.
- **Drop spam, clearly automated content, and obvious abuse.** This is not
  censorship of dissent; it's keeping the archive readable.
- **Trust the visitor's words.** Don't paraphrase. If you must shorten,
  use ellipses or a `context` note explaining what you did.
- **Date what you add.** Use `received` for when you became aware of the
  message, since the visitor's timestamp is unknowable without trackers we
  don't run.

If you're unsure whether to add something, you can skip it. The archive
should reflect care, not completeness.
