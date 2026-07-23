# [ThreatNexus](https://threatnexus.online/) — Nation-State APT Intelligence

![APT Groups](https://img.shields.io/badge/APT%20Groups-67-blue?style=flat-square&logo=github)
![Nation-States](https://img.shields.io/badge/Nation--States-17-red?style=flat-square)
![Analysis Views](https://img.shields.io/badge/Analysis%20Views-6-green?style=flat-square)
![Intel Sources](https://img.shields.io/badge/Intel%20Sources-33-orange?style=flat-square)
![TAXII](https://img.shields.io/badge/STIX%2FTAXII-2.1-9cf?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![TLP](https://img.shields.io/badge/TLP-CLEAR-white?style=flat-square)

🌐 **Live:** [https://threatnexus.online/](https://threatnexus.online/)

---

**ThreatNexus** started with a simple frustration: Most APT references are static.

You look up a threat actor, read through reports or PDFs, and still can't easily answer the questions that matter most for threat hunting and detection engineering:
- Which groups share malware, infrastructure, or tradecraft?
- Which TTPs provide the broadest detection coverage?
- Who is actively targeting my industry right now?
- What's happening across the threat landscape based on intelligence scattered across vendors, CERTs, security researchers, LinkedIn, X, and news sources?

And even when you find the relevant TTPs, the next question is: **So what?**

How do you actually hunt for this activity in your environment?

**Threat intelligence without actionable outcomes is just news.**

ThreatNexus doesn't stop at mapping actors and TTPs. For every technique, it can generate hunting and detection leads, helping analysts translate intelligence into something operational. Think of it as a starting point—a Sigma-style hunting hypothesis that can be adapted to your environment, telemetry, and tooling. It connect threat actors, campaigns, malware, TTPs, vulnerabilities, detections, and intelligence from multiple sources into a single, searchable view.

**The goal isn't just to help you understand adversaries. It's to help you hunt them.**

## What's Inside

ThreatNexus is a threat intelligence platform covering **67 nation-state APT groups and threat clusters across 17 countries**, built for SOC analysts, threat hunters, incident responders, and security leaders. It goes beyond static group profiles:

- **Operational context** — active campaigns, infrastructure patterns, hunt queries
- **Sector-specific risk** — "Who's hunting you?" pivot by industry
- **Regional relevance** — UAE/GCC weighting for Gulf-specific threat assessment
- **Detection linkage** — Sigma, Elastic, and Splunk rule references per technique
- **Live intelligence feeds** — Multiple sources across vendor research, news, government advisories, CVE tracking, and ransomware victim data
- **Machine-readable export** — STIX 2.1 objects over a standards-compliant TAXII 2.1 server, so other platforms can subscribe directly

## Views

The platform consolidated from eight standalone views into **six primary tabs** — Matrix, Sector, and Campaigns are now sub-tabs/aliases rather than separate top-level views, so the same depth is one click closer instead of spread across tabs.

| Tab | Purpose |
|------|---------|
| **Globe** | 3D interactive globe with nation-state markers, target arcs, and floating labels |
| **Cluster** | Graph showing relationships via shared malware, CVEs, and TTPs |
| **Diamond** | Diamond Model cards (Adversary → Capability → Infrastructure → Victim) |
| **Threat Landscape** | Unified executive brief + campaign timeline — CISO/board-ready intelligence brief with a conflict status banner, year-filterable campaign history, and live news matching |
| **Feed** | Live intelligence across 33 curated sources: vendor research blogs, security news, CISA KEV, ransomware victim tracking |
| **Hunt** | Detection and pivot workbench with five sub-tabs: **Detections** (curated hunt queries), **TTP × APT Matrix** (MITRE ATT&CK heatmap with technique reverse-lookup), **IOC Search**, **Sector Pivot** ("who's hunting your industry," ranked by threat score), and **Repositories** (community detection repo links) |

## Data

- **67 threat groups and clusters** (61 active, 6 archived as dormant) across **17 nation-states** (including financially motivated clusters and unknown-attribution groups)
- Every group includes: TTPs (MITRE ATT&CK mapped), malware families, exploited CVEs, campaigns, infrastructure patterns, hunt queries, and member indictments where available
- Canonical naming reconciled against MITRE ATT&CK Groups; vendor personas retained as aliases, not as separate entities
- A single alias, MITRE Group ID, or APT designation resolves to exactly one actor — enforced by an automated lint gate on every data change
- Regional relevance scoring for UAE/GCC
- Neutral attribution policy — Western actors sourced from non-Western intelligence and vice versa
- MITRE ATT&CK Navigator export per group
- Intelligence current as of **June 2026**

## STIX 2.1 / TAXII 2.1 Feed

ThreatNexus exposes its curated actor graph as a **read-only TAXII 2.1 collection** — subscribe once and your platform syncs on its own schedule. No API key required.

- **Discovery:** `https://threatnexus.online/api/taxii2/`
- **Collection:** `threatnexus-apt` (or its UUID, returned by the collections endpoint)
- **Contents:** 61 intrusion-sets, 263 malware families, 121 ATT&CK techniques, 52 exploited CVEs, 729 relationships connecting them — fully linked, not a flat IOC list
- **Standards features:** `match[type]`, `match[id]`, `match[version]`, `added_after` delta sync, cursor-based paging, object manifests
- **Trust markers:** every object is TLP:CLEAR, attributed to ThreatNexus as producer, carries a STIX confidence score mapped from our analyst rating, and references its MITRE ATT&CK Group ID where applicable
- **Stable IDs:** deterministic (UUIDv5) object identifiers, so repeated syncs reconcile instead of duplicating

Step-by-step connection guides for **MISP**, **OpenCTI**, **Microsoft Sentinel**, and plain `curl`/scripts are at [**threatnexus.online/integrate.html**](https://threatnexus.online/integrate.html). A downloadable full STIX bundle is also available there for one-off imports.

## Sources

All data sourced from public, authoritative intelligence — 20+ vendor research organisations cross-referenced per group, reconciled against MITRE ATT&CK Groups:

**Government & Law Enforcement**
CISA · NSA · FBI · DOJ · NCSC-UK · ASD-Australia · CCCS-Canada · CERT-UA · BSI · JPCERT/CC · ENISA · ETDA

**Vendor Research**
CrowdStrike · Mandiant/Google TI · Microsoft MSTIC · Palo Alto Unit 42 · Recorded Future Insikt · Kaspersky Securelist · ESET · SentinelOne · IBM X-Force · Sophos · Cisco Talos · Check Point Research · Proofpoint · Trend Micro · Dragos · Google TAG · Wiz · Hunt.io · Socket.dev · Trellix · Abuse.ch

**Frameworks**
MITRE ATT&CK · STIX 2.1 / TAXII 2.1 · MISP · Microsoft/CrowdStrike Joint Taxonomy (June 2025)

**Live Feeds**
CISA KEV · Ransomware.live · ThreatFox/Abuse.ch · security news sources · government CERT feeds

## Live Intelligence Feed

The Feed tab pulls from **33 continuously updated sources** across five categories:

| Category | Sources | Cycle |
|----------|---------|-------|
| Vendor Research | blogs (Kaspersky, CrowdStrike, Unit 42, Talos, ESET, Sophos, etc.)
| News | (BleepingComputer, THN, Krebs, The Record, Dark Reading, SecurityWeek)
| Government / CERTs | (CISA, NCSC-UK, CERT-EU, JPCERT/CC, CISA News)
| CVE / Vulnerability | (CISA KEV)
| Ransomware | (Ransomware.live — live victim data)

## Detection Integration

ThreatNexus links directly to community detection repositories (under the Hunt tab — Matrix, IOC Search, and Repositories sub-tabs):

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
