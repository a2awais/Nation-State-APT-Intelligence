# Contributing to ThreatNexus

Thank you for contributing to the community's threat intelligence resource. Every contribution improves collective defence.

## Field Reference — APT Group

| Field | Type | Required | Notes |
|-------|------|----------|-------|
| `name` | string | ✓ | Display name (e.g. "Fancy Bear") |
| `apt` | string | — | APT designation (e.g. "APT28") or `""` |
| `aka` | string | — | Aliases separated by ` · ` |
| `country` | string | ✓ | Must match a key in `js/config.js → NATION_COLORS` |
| `agency` | string | ✓ | Attribution unit (e.g. "GRU Unit 26165") |
| `motivation` | string | ✓ | `espionage` \| `financial` \| `destructive` \| `mixed` |
| `active_since` | number | ✓ | Year of first observed activity |
| `last_seen` | number | ✓ | Year of last confirmed activity |
| `confidence` | string | ✓ | `high` \| `medium` \| `low` |
| `sectors` | array | ✓ | Targeted industries |
| `targets` | array | ✓ | Target countries/regions |
| `description` | string | ✓ | Plain text, 2-4 sentences with sourced claims |
| `ttps` | array | — | `[["T1566.001", "Name", "tactic-slug"], ...]` |
| `malware` | array | — | `[["Name", "Type", "Platform"], ...]` |
| `cves` | array | — | `[["CVE-YYYY-XXXXX", CVSS_float, "Product", year], ...]` |
| `detections` | array | — | `[["Source", "Title", "https://url"], ...]` |
| `members` | array | — | `[["Name", "Role", "indicted\|sanctioned\|identified"], ...]` |
| `archived` | boolean | — | `true` if group inactive 3+ years |
| `infra_patterns` | array | — | Plain text descriptions of operational infrastructure |
| `regional_relevance` | object | — | `{"UAE": "high\|medium\|low", "notes": "..."}` |
| `campaigns` | array | — | See Campaign template |
| `hunt_queries` | array | — | `[{"platform":"Sigma\|KQL","description":"...","url":"https://..."}]` |

## Field Reference — Campaign

| Field | Type | Required | Notes |
|-------|------|----------|-------|
| `name` | string | ✓ | Campaign name |
| `start` | string | ✓ | Start date (e.g. "Jan 2026", "2024", "Mar 11 2026") |
| `end` | string | ✓ | End date or `"ongoing"` for active campaigns |
| `sectors` | array | ✓ | Targeted industries |
| `targets` | array | ✓ | Target countries/regions |
| `cves_used` | array | — | CVE IDs exploited in this campaign |
| `source` | string | ✓ | Attribution source (e.g. "Microsoft MSTIC", "CISA") |

## Source Requirements

Every new group or campaign must cite **at least one** public authoritative source:

**Government:**
- CISA, DoJ, FBI, NSA, ODNI (US)
- NCSC-UK, ASD-Australia, CCCS-Canada, GCSB-NZ (Five Eyes)
- CERT-UA, BSI (Germany), ANSSI (France)

**Vendor Research:**
- Mandiant/Google, Microsoft MSTIC, ESET, Palo Alto Unit 42
- CrowdStrike, SentinelOne, Recorded Future, Trellix, Check Point
- Cisco Talos, Sophos, Kaspersky GReAT

**No** anonymous blogs, unverified paste sites, Telegram screenshots, or speculative attribution.

## Quality Standards

- **Accuracy over quantity** — one well-sourced group is better than ten speculative ones
- **Freshness** — update `last_seen` when new activity is confirmed
- **Hunt queries** — only link to real detection rules with working URLs (SigmaHQ, Elastic, Splunk repos)
- **Descriptions** — factual, sourced, no marketing language. State what the group does, not how scary they are.
- **CVEs** — include CVSS score and affected product. Only CVEs confirmed exploited by the group.
