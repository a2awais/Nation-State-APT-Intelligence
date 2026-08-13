# Contributing to ThreatNexus

Thanks for wanting to help. This project is one person's corpus, and it gets better
the more practitioners push back on it.

**Read this first:** this repository contains **no platform source code**. ThreatNexus
runs as a hosted service and the pipeline is proprietary. What you contribute here is
**intelligence, corrections, and documentation** — which is the part that actually
determines whether the platform is worth using.

---

## What we're looking for

**High value, always welcome:**

| Contribution | What makes it accepted |
|---|---|
| **New threat actor** | A publicly reported nation-state or state-aligned group not yet tracked, with at least one primary source (vendor research, CERT advisory, indictment) |
| **New campaign** | A named operation with dated reporting and an identified or credibly suspected actor |
| **Corrections** | Wrong attribution, stale "last seen", misattributed malware, an alias mapped to the wrong actor. **These are the most valuable submissions we receive.** |
| **Alias reconciliation** | A vendor persona that is the same cluster as an existing entry, with the reporting that establishes the overlap |
| **Source references** | A government advisory, indictment, or vendor report that should be cited on an existing dossier |
| **TTP / malware / CVE additions** | Technique or tooling attributed to a tracked actor in published reporting |
| **Dormancy signals** | Evidence an actor should be archived, or reactivated |
| **Documentation** | Clarity fixes, methodology questions, integration guides |

**Not accepted, and why:**

- ❌ **Anything non-public.** No client data, no incident details from your day job,
  no TLP:AMBER/RED material, nothing under NDA. This is the hard line and there are
  no exceptions.
- ❌ **Unsourced claims.** "I heard APT-X is behind this" is not an intelligence
  submission. Every factual claim needs a citable public source.
- ❌ **Speculative attribution.** Circumstantial pattern-matching without reporting
  behind it. Precision over recall is the project's explicit policy.
- ❌ **Live indicators as a bulk feed.** Individual IOCs tied to a dossier are fine;
  bulk blocklists are not what this corpus is.
- ❌ **Pull requests against platform code.** There isn't any here.

---

## How to submit

### 1. Open an issue using the right template

- **New Actor** · **New Campaign** · **Correction** · **Source Reference** ·
  **Documentation**

One submission per issue. A single issue proposing six actors cannot be partially
accepted, and it will be asked to be split.

### 2. Include the evidence

Every submission needs:

- **At least one primary source URL** — vendor research, CERT/government advisory,
  court document, or peer-reviewed work. News coverage *of* a report is acceptable
  as a pointer, but link the report itself where it exists.
- **The date of the reporting**, not the date you found it.
- **What the source actually says**, in your words — a short quote or paraphrase
  showing the claim is in the source rather than inferred from it.
- **Your confidence** and why: what would change your mind?

For a new actor, also include: known aliases and who assigns them, suspected
sponsor and the basis for that, targeted sectors and regions, observed malware, and
MITRE ATT&CK technique IDs where reporting supports them.

**A note on sourcing standard.** The bar is not "is this plausible" — it is "does a
named public source state this." Contributions that meet that bar get reviewed
quickly. Contributions that don't get one round of questions and then get closed.
That's not gatekeeping for its own sake; a corpus that admits unsourced claims
stops being worth citing.

### 3. Sign off

Add this line to your issue or PR:

```
Signed-off-by: Your Name <your@email.example>
```

By signing off you certify that:

1. You have the right to submit this material and to license it under the project's
   terms (CC BY 4.0 for intelligence and documentation, Apache-2.0 for code samples).
2. **The material is derived from publicly available sources.** It is not
   confidential, client-privileged, classified, or subject to restricted handling
   (TLP:AMBER or above).
3. You understand the submission and your attribution will be public and permanent.

There is **no CLA and no copyright assignment.** You keep your copyright. Inbound
licence equals outbound licence — nothing more.

---

## What happens next

Every submission goes through the same review path the platform's own automated
pipeline goes through. Nothing skips it, including submissions from the maintainer.

```
  submission
      │
      ▼
  [1] Triage           — scope, duplicates, sourcing bar        (usually 3–7 days)
      │
      ▼
  [2] Verification     — sources checked at origin; claims must appear
      │                   in the cited text, not be inferred from it
      ▼
  [3] Reconciliation   — canonical naming against MITRE ATT&CK Groups;
      │                   alias collision and namesake checks
      ▼
  [4] Human approval   — accepted, revised, or declined with reasons
      │
      ▼
  [5] Published        — appears on threatnexus.online and in the
                          STIX/TAXII export on the next data build
```

**Expect questions.** Most accepted submissions go through at least one round. That
is the review working, not a rejection.

**Declines get reasons.** If a submission doesn't make it, you'll be told which step
it failed and what would change the answer. A decline for insufficient sourcing is
not a decline forever — reopen it when better reporting exists.

**Timelines are best-effort.** This is maintained by one person alongside a full-time
job. Triage is usually within a week; a complex new-actor submission may take longer.
If something has gone quiet for three weeks, ping the issue.

---

## Credit

Accepted contributions are credited. Specifically:

- Your name (or handle, your choice) is listed in `CREDITS.md` in this repository.
- Substantive contributions — a new actor, a significant correction, a campaign —
  are credited on the affected dossier on the live site.
- You can ask to be credited anonymously, or not at all. Say so in the issue.

Credit is for **accepted** contributions. Opening an issue is not itself a
contribution credit, and volume is not the metric — one well-sourced correction to a
wrong attribution is worth more to this project than twenty additions.

---

## Reporting problems

- **Security vulnerability** → `SECURITY.md` or
  `https://threatnexus.online/.well-known/security.txt`. Please do not open a public
  issue for a live vulnerability.
- **Wrong or harmful attribution** → open a Correction issue and mark it urgent. A
  false attribution is treated as a defect with priority over any feature work.
- **You are named on a dossier and believe it is wrong** → contact the maintainer
  directly via the address in `SECURITY.md`. This will be looked at promptly and in
  good faith.
- **Licensing question not answered by `LICENSES.md`** → open an issue. An unclear
  licence is a bug in the licence, and it gets fixed in the file rather than settled
  in a private reply.

---

## Conduct

Be direct, be technical, be kind. Disagreement about attribution is the normal
condition of this field and is welcome — the corpus improves because people argue
with it. Personal hostility is not, and will end the conversation.

---

## Licensing summary

Contributions are accepted **inbound = outbound**:

| You contribute | It is published under |
|---|---|
| Intelligence, dossier content, corrections | CC BY 4.0 |
| Documentation | CC BY 4.0 |
| Code samples, schemas, integration examples | Apache-2.0 |

Full terms, and the notice on third-party intelligence ThreatNexus does **not** own:
[`LICENSES.md`](LICENSES.md).
