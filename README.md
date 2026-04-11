# [ThreatNexus](https://threatnexus.onilne/) — Nation-State APT Intelligence

![APT Groups](https://img.shields.io/badge/APT%20Groups-52-blue?style=flat-square&logo=github)
![Nation-States](https://img.shields.io/badge/Nation--States-14-red?style=flat-square)
![Analysis Views](https://img.shields.io/badge/Analysis%20Views-8-green?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![TLP](https://img.shields.io/badge/TLP-CLEAR-white?style=flat-square)

🌐 **Live:** [https://threatnexus.onilne/](https://threatnexus.onilne/)

---

**ThreatNexus** started from a simple frustration — existing APT references are static. You look up a group, read a PDF, and still can't answer the questions that actually matter for detection: who shares tooling with who, which technique covers the most actors, and who is actively hunting your industry right now. Built this to answer those questions in one place, and opening it to the threat intelligence and hunting community to use and build on.

## What's Inside

ThreatNexus is a threat intelligence platform covering **52 nation-state APT groups across 14 countries**, built for SOC analysts, threat hunters, incident responders, and security leaders. It goes beyond static group profiles:

- **Operational context** — active campaigns, infrastructure patterns, hunt queries
- **Sector-specific risk** — "Who's hunting you?" pivot by industry
- **Regional relevance** — UAE/GCC weighting for Gulf-specific threat assessment
- **Detection linkage** — Sigma, Elastic, and Splunk rule references per technique
- **Live intelligence feeds** — CISA KEV, security news RSS, ransomware victim tracking

## Views

| View | Purpose |
|------|---------|
| **Globe** | 3D interactive globe with nation-state markers, target arcs, and floating labels |
| **Cluster** | D3 force-directed graph showing relationships via shared malware, CVEs, and TTPs |
| **Diamond** | Diamond Model cards (Adversary → Capability → Infrastructure → Victim) |
| **Matrix** | MITRE ATT&CK heatmap with technique reverse-lookup and detection repo links |
| **Sector** | Industry pivot — select your sector, see every group targeting it ranked by threat score |
| **Campaigns** | Gantt-style timeline of active and historical campaigns with year filtering |
| **Brief** | Executive intelligence brief for CISO/board consumption with conflict status banner |
| **Feed** | Live data from CISA KEV, security news RSS, ransomware.live, and curated intel sources |

## Data

- **52 threat groups** across **14 nation-states**
- Every group includes: TTPs (MITRE ATT&CK mapped), malware families, exploited CVEs, campaigns, infrastructure patterns, hunt queries, and member indictments
- Regional relevance scoring for UAE/GCC
- MITRE ATT&CK Navigator export per group

## Sources

All data is sourced from public, authoritative intelligence:

- **Government:** CISA, NSA, FBI, DOJ, NCSC-UK, ASD-Australia, CCCS-Canada, CERT-UA
- **Vendor Research:** Mandiant/Google, Microsoft MSTIC, ESET, Palo Alto Unit 42, CrowdStrike, SentinelOne, Trellix, Check Point, Cisco Talos, kaspersky
- **Frameworks:** MITRE ATT&CK, MISP
- **Live Feeds:** CISA KEV, NVD, ransomware.live, Abuse.ch

## Detection Integration

ThreatNexus links directly to community detection repositories:

- [SigmaHQ](https://github.com/SigmaHQ/sigma) — Σ button on every TTP in group dossiers
- [Elastic Detection Rules](https://github.com/elastic/detection-rules) — Matrix reverse-lookup
- [Splunk Security Content](https://github.com/splunk/security_content) — Matrix reverse-lookup
- [Hayabusa](https://github.com/Yamato-Security/hayabusa) — Feed intel sources

## Disclaimer

Attribution is complex. This tool aggregates publicly available intelligence and should not be treated as definitive attribution. Groups change toolsets, share infrastructure, and conduct false-flag operations. Information may be incomplete, outdated, or wrong. Always corroborate with multiple sources.

**TLP:CLEAR** — This project contains no classified or restricted information.

## Author

**Awais Munir** — [Linkedin](https://www.linkedin.com/in/iawais/)

Built for the community. Stay vigilant.
