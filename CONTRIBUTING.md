# Contributing to ThreatNexus

ThreatNexus tracks 67 nation-state APT groups across 17 countries — every dossier
mapped to MITRE ATT&CK, cited to government advisories and vendor research, and
reconciled so that one alias resolves to exactly one actor. It's used by threat
hunters, detection engineers and incident responders, and it's free.

**It gets better when practitioners contribute to it.** You work incidents, read
vendor reporting, and notice things the corpus doesn't have yet. That's exactly what
this process is for.

---

## What you can contribute

**Threat actors.** A nation-state or state-aligned group that should be tracked, or
new detail on one that already is — aliases and who assigns them, sponsor,
targeting, ATT&CK-mapped TTPs.

**Campaigns.** Named operations, their timeline, their targets, and the actor behind
them.

**Malware and tooling.** Families and utilities attributed to a tracked actor,
including capability notes and how the attribution was established.

**Intelligence and corrections.** New advisories or research that should be cited on
an existing dossier. Alias reconciliations where two vendor personas turn out to be
one cluster. Dormancy signals. Fresh CVEs under active exploitation.

**Corrections are the most valuable submissions we receive.** A wrong attribution
caught early is worth more to this corpus than ten additions — if you spot one, say
so, and it goes to the front of the queue.

---

## How to submit

**Open an issue** using the template that fits — New Actor, New Campaign, Malware,
or Correction. One subject per issue keeps review fast.

**Bring the source.** Every submission carries:

- **A link to the reporting** — vendor research, CERT or government advisory, court
  filing, or peer-reviewed work.
- **The date of the reporting.**
- **What the source says**, briefly, in your words — enough to show the claim is in
  the source.
- **Your read on confidence**, and what would change it.

For a new actor, the more of this you have the faster it moves: aliases and their
origin, suspected sponsor, targeted sectors and regions, observed malware, and ATT&CK
technique IDs.

That's the whole bar. **If a named public source states it, it's reviewable.** Rough
notes with a good link beat a polished writeup without one — send it and we'll work
it out together.

**Sign off** with `Signed-off-by: Your Name <you@example.com>`, confirming you have
the right to share the material, that it comes from public sources, and that it isn't
client-confidential or restricted-handling. You keep your copyright — there's no CLA
and no assignment.

---

## How it gets in

Everything follows the same path, including the maintainer's own work:

```
  Your submission
        │
   ▶ Triage           scope and sourcing, usually within a week
        │
   ▶ Verification     sources checked at origin — claims must appear
        │              in the cited text
        │
   ▶ Reconciliation   canonical naming against MITRE ATT&CK Groups,
        │              alias and namesake collision checks
        │
   ▶ Review           accepted, refined, or discussed further
        │
   ▶ Live             on threatnexus.online and in the STIX/TAXII
                       export on the next data build
```

Expect a conversation. Most accepted submissions go through a round of questions —
that's the review doing its job, and it's usually where the entry gets sharper.

If something doesn't make it, you'll be told which step it stopped at and what would
change the answer. That's rarely permanent: reopen it when stronger reporting lands.

Timelines are best-effort — this is maintained by one person alongside a full-time
job. Triage is usually inside a week. If an issue has gone quiet for three weeks,
give it a nudge.

---

## Credit

Accepted contributions are credited by name or handle — on the dossier you improved,
and in the project credits. Prefer to stay anonymous? Say so in the issue and that's
respected.

Credit follows impact, not volume. One well-sourced correction to a wrong attribution
counts for more here than twenty additions.

---

## Good to know

**This repository is the community and documentation home.** ThreatNexus runs as a
hosted service and its source isn't published here, so contributions are intelligence
contributions rather than code — which is the part that determines whether the
platform is worth using.

**Keep it public-source.** Everything in ThreatNexus is TLP:CLEAR and traceable to a
citable source, which is what makes it safe to redistribute and worth citing. Please
don't send anything client-confidential, under NDA, or marked TLP:AMBER or above.

**Something wrong on a dossier about you or your organisation?** Contact the
maintainer directly — see
[security.txt](https://threatnexus.online/.well-known/security.txt). It will be
looked at promptly and in good faith.

**Found a security vulnerability in the platform?** Same contact — please not a
public issue.

---

## Licence

Contributions are published under the project's terms: **CC BY 4.0** for intelligence
and documentation. Inbound equals outbound — nothing more is asked of you. See the
[README](README.md#licence).
