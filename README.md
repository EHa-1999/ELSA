# ELSA

**Electronic Letters & Storage Archive.** A demo of e-mail archiving in XENA: every message goes into the register and the object storage automatically, and staff simply read it in their own mail program via IMAP.

ELSA is part of XENA, alongside the storage demo, MIRA (the assistant in the office suite) and TINA (the search portal for citizens).

> A demo, not a product. People, messages, addresses and numbers are invented.

Nederlandse versie: [README.nl.md](README.nl.md)

## What the demo shows

| View | What you see |
|---|---|
| **Mailbox** | A mail program that reads from ELSA via IMAP. For each message the choice business or personal, with ten days to decide, completing the metadata and encryption. Deleting a business message removes it from the folder, but it stays archived. |
| **Flow** | How a message travels via Exchange Online, a transport rule, Kafka and a small bridge into Nextcloud, and from there into the register, the object storage and the search index within a second, with no copy left in Exchange. |
| **Filters** | Sieve filters that run in ELSA itself, with the actions that are not allowed because they would bypass the separation. |
| **Address book** | A municipal address book in which everyone decides whether and with which details they appear, shared via CardDAV. |
| **Keys** | Personal messages are encrypted with a personal key. Only the municipal secretary can grant access or delegate that power, and everything is logged. |
| **Architecture** | The layers from workplace to the XENA Nextcloud stack, the steps per action, and the open points. One message in object storage, with the IMAP server and Nextcloud Files as two access routes. |
| **Technology** | Three ways to run IMAP next to WebDAV, a comparison of Apache James, Stalwart and Dovecot, what needs to be built, and the open standards. |
| **Growth path** | Five steps, from archiving and search next to Exchange to working without Exchange. |

The buttons at the top let you jump ahead in time to see what happens after ten days.

## Use

Open `index.html` in a browser. No server is needed. Languages: Dutch, German, English and French; `#de`, `#en` or `#fr` after the address selects the language for that one link.

## Build

```
python3 build.py
```

writes `index.html` and `ELSA - v<N>.html`. The version number is in `VERSION`.

## Licence

EUPL-1.2, see `LICENSE`.
