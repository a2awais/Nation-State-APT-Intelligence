# [ThreatNexus](https://threatnexus.online/) — Nation-State APT Intelligence

![APT Groups](https://img.shields.io/badge/APT%20Groups-68-blue?style=flat-square&logo=github)
![Nation-States](https://img.shields.io/badge/Nation--States-17-red?style=flat-square)
![Analysis Views](https://img.shields.io/badge/Analysis%20Views-8-green?style=flat-square)
![Intel Sources](https://img.shields.io/badge/Intel%20Sources-33-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![TLP](https://img.shields.io/badge/TLP-CLEAR-white?style=flat-square)

🌐 **Live:** [https://threatnexus.online/](https://threatnexus.online/)

---

**ThreatNexus** started from a simple frustration — existing APT references are static. You look up a group, read a PDF, and still can't answer the questions that actually matter for detection: who shares tooling with who, which technique covers the most actors, and who is actively hunting your industry right now. Built this to answer those questions in one place, and opening it to the threat intelligence and hunting community to use and build on.

## What's Inside

ThreatNexus is a threat intelligence platform covering **68 nation-state APT groups and threat clusters across 17 countries**, built for SOC analysts, threat hunters, incident responders, and security leaders. It goes beyond static group profiles:

- **Operational context** — active campaigns, infrastructure patterns, hunt queries
- **Sector-specific risk** — "Who's hunting you?" pivot by industry
- **Regional relevance** — UAE/GCC weighting for Gulf-specific threat assessment
- **Detection linkage** — Sigma, Elastic, and Splunk rule references per technique
- **Live intelligence feeds** — 33 sources across vendor research, news, government advisories, CVE tracking, and ransomware victim data

## Views

| View | Purpose |
|------|---------|
| **Globe** | 3D interactive globe with nation-state markers, target arcs, and floating labels |
| **Cluster** | D3 force-directed graph showing relationships via shared malware, CVEs, and TTPs |
| **Diamond** | Diamond Model cards (Adversary → Capability → Infrastructure → Victim) |
| **Matrix** | MITRE ATT&CK heatmap with technique reverse-lookup and detection repo links |
| **Sector** | Industry pivot — select your sector, see every group targeting it ranked by threat score |
| **Campaigns** | Gantt-style timeline of active and historical campaigns with year filtering and live news matching |
| **Brief** | Executive intelligence brief for CISO/board consumption with conflict status banner |
| **Feed** | Live intelligence across 33 curated sources: vendor research blogs, security news, CISA KEV, ransomware victim tracking |

## Data

- **68 threat groups and clusters** across **17 nation-states** (including financially motivated clusters and unknown-attribution groups)
- Every group includes: TTPs (MITRE ATT&CK mapped), malware families, exploited CVEs, campaigns, infrastructure patterns, hunt queries, and member indictments where available
- Regional relevance scoring for UAE/GCC
- Neutral attribution policy — Western actors sourced from non-Western intelligence and vice versa
- MITRE ATT&CK Navigator export per group
- Intelligence current as of **May 2026**

## Sources

All data sourced from public, authoritative intelligence — 20+ vendor research organisations cross-referenced per group:

**Government & Law Enforcement**
CISA · NSA · FBI · DOJ · NCSC-UK · ASD-Australia · CCCS-Canada · CERT-UA · BSI · JPCERT/CC · ENISA

**Vendor Research**
CrowdStrike · Mandiant/Google TI · Microsoft MSTIC · Palo Alto Unit 42 · Recorded Future Insikt · Kaspersky Securelist · ESET · SentinelOne · IBM X-Force · Sophos · Cisco Talos · Check Point Research · Proofpoint · Trend Micro · Dragos · Google TAG · Wiz · Hunt.io · Socket.dev · Trellix · Abuse.ch

**Frameworks**
MITRE ATT&CK · MISP · Microsoft/CrowdStrike Joint Taxonomy (June 2025)

**Live Feeds**
CISA KEV · Ransomware.live · ThreatFox/Abuse.ch · 6 security news sources · 5 government CERT feeds

## Live Intelligence Feed

The Feed tab pulls from **33 continuously updated sources** across five categories:

| Category | Sources | Cycle |
|----------|---------|-------|
| Vendor Research | 20 blogs (Kaspersky, CrowdStrike, Unit 42, Talos, ESET, Sophos, etc.) | Every ~1.5 hrs |
| News | 6 (BleepingComputer, THN, Krebs, The Record, Dark Reading, SecurityWeek) | Every 30 min |
| Government / CERTs | 5 (CISA, NCSC-UK, CERT-EU, JPCERT/CC, CISA News) | Every 30 min |
| CVE / Vulnerability | 1 (CISA KEV — live JSON) | Every 30 min |
| Ransomware | 1 (Ransomware.live — live victim data) | Every 30 min |

## Detection Integration

ThreatNexus links directly to community detection repositories:

- [SigmaHQ](https://github.com/SigmaHQ/sigma) — Σ button on every TTP in group dossiers
- [Elastic Detection Rules](https://github.com/elastic/detection-rules) — Matrix reverse-lookup
- [Splunk Security Content](https://github.com/splunk/security_content) — Matrix reverse-lookup
- [Hayabusa](https://github.com/Yamato-Security/hayabusa) — Windows event log hunting rules

## Disclaimer

Attribution is complex. This tool aggregates publicly available intelligence and should not be treated as definitive attribution. Groups change toolsets, share infrastructure, and conduct false-flag operations. Information may be incomplete, outdated, or wrong. Always corroborate with multiple sources.

**TLP:CLEAR** — This project contains no classified or restricted information.

## Author

**Awais Munir** — [LinkedIn](https://www.linkedin.com/in/iawais/)

Built for the community. Stay vigilant.
