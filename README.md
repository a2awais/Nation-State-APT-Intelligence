# [ThreatNexus](https://threatnexus.online) — Nation-State APT Threat Intelligence

**Free. No login.** 67 nation-state APT groups across 17 countries — mapped to MITRE
ATT&CK, linked to detections, and updated continuously from vendor research, CERT
advisories and government reporting.

### 🌐 **[threatnexus.online](https://threatnexus.online/)**

![APT Groups](https://img.shields.io/badge/APT%20Groups-67-blue?style=flat-square)
![Nation-States](https://img.shields.io/badge/Nation--States-17-red?style=flat-square)
![Intel Sources](https://img.shields.io/badge/Intel%20Sources-41-orange?style=flat-square)
![STIX/TAXII](https://img.shields.io/badge/STIX%2FTAXII-2.1-9cf?style=flat-square)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey?style=flat-square)
![TLP](https://img.shields.io/badge/TLP-CLEAR-white?style=flat-square)

---

## The problem it solves

Most APT references are static. You look up Sandworm, APT29 or Lazarus, read a PDF,
and still can't answer the questions that decide what you do next:

- **Which groups share malware, infrastructure or tradecraft?**
- **Which ATT&CK techniques give the broadest coverage across the actors that matter
  to me?**
- **Who is targeting my sector right now?**
- **What changed this week**, across twenty vendor blogs and five CERT feeds?

And once you have the technique — *so what?* How do you hunt it in your telemetry?

**Threat intelligence without an operational outcome is just news.** ThreatNexus
connects threat actors, campaigns, malware, ATT&CK techniques, CVEs and live reporting
into one searchable view, and carries every technique through to a hunting lead you
can adapt.

## Capabilities

**Threat actor intelligence**
67 nation-state and state-aligned groups. Each dossier carries aliases and who assigns
them, sponsor, targeted sectors and regions, ATT&CK-mapped TTPs, malware families,
exploited CVEs, campaign history, infrastructure patterns and named indictments —
with the government advisories and vendor research behind each claim.

**Pivots that answer real questions**
*Who's hunting my industry?* — every actor targeting your sector, ranked. *Which
technique buys me the most coverage?* — a TTP × APT heatmap with technique
reverse-lookup. *Who else uses this malware?* — a relationship graph over shared
tooling, shared CVEs and shared tradecraft. Plus Diamond Model cards per actor and an
interactive globe of targeting geography.

**Live intelligence feed**
41 continuously polled sources — vendor research, security news, government CERT
advisories, CISA KEV and ransomware victim data — deduplicated, clustered by story,
severity-ranked and attributed to actors where the reporting supports it. Exportable
as a TLP:CLEAR advisory.

**PRISM — indicator enrichment**
Submit a domain, IP, hash or URL and get a single assembled picture: registration and
hosting, passive DNS, certificate history, sandbox and multi-engine verdicts,
reputation and abuse signals, plus any prior sighting inside the ThreatNexus corpus.
Every datum is labelled with the provider that supplied it and when it was observed.
Infrastructure facts never move the malice verdict, and *benign* is never asserted
without positive evidence — absence of evidence returns Unknown, not clean.

**Threat Landscape**
Board-ready executive brief and campaign timeline, with conflict status and
year-filterable history.

**Machine-readable access**
STIX 2.1 objects over a read-only TAXII 2.1 server. Point any compliant TIP or SIEM at
the discovery endpoint and subscribe — no account required.

## Why trust the data

- **One actor, one identity.** Aliases, MITRE Group IDs and APT designations each
  resolve to exactly one actor, enforced automatically on every data change. Vendor
  personas are aliases, not duplicate entries.
- **Precision over recall on attribution.** An actor is linked to a report only when
  the text uses the name *as an actor name*. A missing link costs you nothing; a wrong
  one costs the platform its reason to exist.
- **Sourced, not asserted.** Every dossier cites its advisories, research and
  indictments.
- **Reviewed by a human before publication.** Automation proposes. A person approves.
- **Dormancy is recorded, not hidden** — inactive actors are archived rather than left
  implying they're current.

Intelligence current as of **June 2026**.

## Detection

Every technique in a dossier links through to community detection content —
[SigmaHQ](https://github.com/SigmaHQ/sigma),
[Elastic Detection Rules](https://github.com/elastic/detection-rules),
[Splunk Security Content](https://github.com/splunk/security_content) and
[Hayabusa](https://github.com/Yamato-Security/hayabusa).

Companion repository: **[a2awais/Threat-Hunting](https://github.com/a2awais/Threat-Hunting)**
— CQL and KQL hunting queries mapped to MITRE ATT&CK.

## Sources

Compiled from public reporting — 20+ research organisations cross-referenced per
actor, reconciled against MITRE ATT&CK Groups.

**Government & law enforcement** — CISA · NSA · FBI · DOJ · NCSC-UK · ASD · CCCS ·
CERT-UA · BSI · JPCERT/CC · ENISA · ETDA

**Vendor research** — CrowdStrike · Mandiant/Google TI · Microsoft MSTIC · Unit 42 ·
Recorded Future · Kaspersky · ESET · SentinelOne · IBM X-Force · Sophos · Cisco Talos ·
Check Point · Proofpoint · Trend Micro · Dragos · Google TAG · Wiz · Hunt.io ·
Socket.dev · Trellix · abuse.ch

**Standards** — MITRE ATT&CK · STIX 2.1 / TAXII 2.1 · Diamond Model · MISP

> ThreatNexus is **not affiliated with, sponsored by or endorsed by** any organisation
> named above. They appear because their published research is cited.

---

## About this repository

This is the **community and documentation home** for ThreatNexus. The platform runs as
a hosted service and its source code is not published — but **the intelligence is
open**: free to use, redistribute and build on under CC BY 4.0, and available
machine-readable over TAXII 2.1.

**Contributions here are intelligence contributions.** New actors, new campaigns,
corrections, alias reconciliations and source references are welcome, reviewed against
public sources, and credited.

→ **[How to contribute](CONTRIBUTING.md)**

## Licence

**Content — CC BY 4.0.** The dossiers, their structure and analysis, the STIX/TAXII
exports and this documentation are free to use and redistribute, including
commercially. Credit ThreatNexus and don't imply endorsement.

**The underlying reporting is not ours.** Dossiers are compiled from third-party
government and vendor research; those reports remain the property of their authors and
are governed by their own terms. CC BY 4.0 covers the compilation, structure and
analysis — not the source material.

**Platform source is proprietary** and not published here.

## Disclaimer

Attribution is hard. This platform compiles publicly available intelligence and
**should not be treated as definitive attribution.** Groups change toolsets, share
infrastructure and run false-flag operations. Always corroborate against primary
sources before acting.

**TLP:CLEAR** — contains no classified or restricted information.

---

Built and maintained by **Awais Munir** —
[LinkedIn](https://www.linkedin.com/in/iawais/) ·
[GitHub](https://github.com/a2awais)

*Built for the community. Stay vigilant.*
