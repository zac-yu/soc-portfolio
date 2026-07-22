# Repository Security and Privacy

This is a public portfolio repository. Before committing any file or screenshot:

- Remove passwords, recovery codes, tokens, API keys and license keys.
- Remove customer names, internal tickets, email addresses and personal information.
- Avoid exposing real tenant IDs, subscription IDs, public IPs and device serial numbers.
- Do not upload VM disk images, packet captures containing private traffic, raw production logs, or configuration backups containing secrets.
- Use fictional names and lab-only data in demonstrations.
- Crop screenshots to the relevant evidence and blur sensitive fields.
- Review staged changes with `git diff --staged` before every push.

The IP range `10.10.10.0/24` shown in this repository is an RFC1918 private lab range.

