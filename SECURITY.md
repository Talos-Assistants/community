# Security Policy

## Do not open a public issue for a vulnerability

This repository has public issues and public discussions. Filing a vulnerability in either one
publishes it to everyone, including to whoever would use it, before there is a fix to upgrade to.

## How to report one

1. Preferred: [report it privately through GitHub](https://github.com/Talos-Assistants/community/security/advisories/new).
   Private reporting keeps it between you and us until an advisory is published.
2. Or email `contact@talosassistants.com` with `SECURITY` in the subject.

Please include what you were running, what you did, and what it let you do. A proof of concept is
welcome but not required. A clear description of the flaw is enough to start.

## What happens next

- We aim to acknowledge a report within 3 working days. Talos is built by a very small team, so treat
  that as a target rather than a contractual SLA.
- We will tell you whether we consider it a vulnerability, and why, either way.
- If it is one, we will agree a disclosure timeline with you. By default, details become public once a
  fixed release exists and people have had a reasonable chance to upgrade.
- You will be credited in the advisory unless you would rather not be.

## What is in scope

Anything that ships as part of Talos:

- **Talos Brain**, the self-hosted service, including its API and licence verification.
- **Talos Studio** and the CLI.
- **The hub** at `hub.talosassistants.com`: accounts, licence issuing, the signed registry, downloads.
- **The website** at `talosassistants.com`.

We are particularly interested in:

- Forging or replaying a signed licence or a signed registry catalog, or getting a brain to accept
  unsigned or altered artifact bytes.
- Anything that reaches another account's data on the hub, or escalates to admin.
- Anything that lets a brain be reached from outside the network it was meant to stay on.

## Out of scope

- Automated scanner output with no demonstrated impact.
- Missing hardening headers or TLS configuration ratings with nothing exploitable behind them.
- Social engineering, physical access, and denial of service by volume.
- Anything requiring a machine the attacker already fully controls. Community is software you run
  yourself, so modifying your own install is not a vulnerability.

## Please do not

Test against anyone else's install or account, run automated scans against `hub.talosassistants.com`,
or access data that is not yours. Test against your own self-hosted brain. That is what it is for.
