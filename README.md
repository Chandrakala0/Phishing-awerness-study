# Phishing Awareness Study (CYB 616)

A graduate group project at Grand Valley State University examining how
credential-harvesting phishing campaigns are built, and — more importantly — how
organizations detect and defend against them.

> **Ethics & scope:** Conducted entirely in an isolated virtual lab for
> educational purposes. No real individuals were targeted and no genuine
> credentials were collected (all inputs used during testing were fabricated for
> demonstration). This repository contains the written study only — no runnable
> attack code and no cloned login pages.

## 📄 Full report

See **[report.pdf](report.pdf)** for the complete writeup: abstract, tools,
methodology, findings, and mitigation strategies.

## Summary

Phishing succeeds by exploiting human trust under urgency rather than a software
flaw. This study walks through the anatomy of a simulated campaign and focuses on
the defender's side.

**What the simulation showed**
- Convincing look-alike login pages and brand-styled "security alert" emails take
  very little effort to produce, so users cannot be the only line of defense.
- A single form submission can expose a password, IP address, and coarse
  geolocation at once.
- The real exploit is urgency ("secure your account now"), not a technical trick.

**Defenses that break the attack**
- **Email authentication (SPF, DKIM, DMARC)** — stops forged sender domains.
- **MFA / passkeys** — make a stolen password useless on its own.
- **User awareness + one-click reporting** — train for the urgency pattern and
  make reporting easy.
- **SIEM anomalous-login detection** — catch the follow-on login (impossible
  travel, unexpected ISP or location).

## Tools studied (named for context, not provided here)

Shellphish-style template framework, Ngrok, PHP, Kali Linux.

## Author

Chandrakala Nenavath — M.S. Cybersecurity, GVSU (expected Dec 2026)
