# SOS Partnership — STATUS

**Last updated:** 2026-04-18
**Phase:** Proposal drafting (pre-send)
**Partner:** SOS Children's Villages India
**Relationship:** Active — MNTEST customer since 2012

---

## Current state

Draft proposal is ready for Steven's review. Not yet sent to SOS.

### Canonical deliverable

| File | What it is |
|------|------------|
| [proposal-2026-04-17-v2.md](proposal-2026-04-17-v2.md) | **Current proposal draft (Markdown source)** — all edits applied |
| [proposal-2026-04-17-v2.pdf](proposal-2026-04-17-v2.pdf) | **Current proposal (PDF, rendered for delivery)** |
| [proposal.css](proposal.css) | Design-system-based stylesheet (Libre Baskerville + IBM Plex Sans, navy-purple cover gradient with pale sky blue accents, thread-colored section headings) |

### Generate the PDF

```bash
pandoc proposal-2026-04-17-v2.md -o proposal-2026-04-17-v2.pdf \
  --pdf-engine=weasyprint \
  --css=proposal.css \
  --standalone
```

---

## Pricing (current, as of 2026-04-18)

Modeled at 800 students / year. 50 coworkers.

### Line-item retail

| Item | Annual |
|------|--------|
| Xavigate Map | $97/student × 800 = $77,600 |
| Training course | $599/coworker × 50 = $29,950 |
| Interpretation guides | $5,500 |
| Webinars (8/yr @ $750) | $6,000 |
| Research partnership | $5,000 |
| Coordinator support | included |
| **Annual retail** | **$124,050** |
| One-time custom build (Y1) — retail | $15,000 |

### SOS partner price (single site license)

| | Amount |
|---|--------|
| Annual site license (unlimited students, unlimited coworkers) | **$20,000/yr** |
| One-time custom build (Y1) — reduced from $15K retail | **$7,500** |
| **Year 1 total** | **$27,500** |
| **Year 2+** | **$20,000/yr** |

**MNTEST is separate and unchanged** — continues at preferred partner rate (not mentioned explicitly in the proposal).

---

## What the proposal covers

1. **Xavigate Map (SOS Edition)** — personalized 14-page PDF per student. Coordinator enters intake → system does research, eligibility checks, shortlisting → report out. Days → minutes.
2. **Careers / tasks / activities database** — 3,000+ items across 19 MN×MI dimensions
3. **Higher-education database** — 91,375 institutions, 245,186 programs, 8,426 NAAC, 11,382 NIRF, 12,041 placements
4. **Scholarship eligibility** — PM CARES, Central Sector, PMSS, SC/ST/OBC/Min, Pragati, Saksham, 6 state orphan schemes, Top-Class SC
5. **SOS data integration** — SOS's 14-year college knowledge incorporated as SOS-verified layer (part of Y1 custom build)
6. **Training course** — 6-hour self-paced, unlimited coworker access
7. **Interpretation guides** — PDF + PPT for coordinators
8. **Webinars** — 4 coworker-facing + 4 children-facing per year, Steven personally
9. **Research partnership** — longitudinal MN-effectiveness study, joint publication Month 12
10. **Coordinator support channel** — included

---

## Key framing choices (lock in before sending)

| Choice | State |
|--------|-------|
| MNTEST kept separate from new proposal stack | ✓ |
| MNTEST rate not explicitly stated (avoids locking a future increase) | ✓ |
| No "90% off" annotations in line items — clean retail table | ✓ |
| Database numbers factual, no superlatives or origin-story puffery | ✓ |
| Research partnership priced as service MNI provides (not a favor SOS grants) | ✓ |
| Paralipsis removed throughout (no "not a vendor", "not custom-built", etc.) | ✓ |
| Time-savings + no-commission differentiators called out in summary + §4 + §9 | ✓ |
| No hard dates in "Next steps" | ✓ |
| Cover: navy→purple Hero gradient with pale sky blue accents (no orange/red on blue) | ✓ |

---

## Today's changes (2026-04-17 → 2026-04-18)

- Full proposal structure written: summary (Part One) + detailed (Part Two, 11 sections)
- Design-system PDF pipeline set up (pandoc + weasyprint + proposal.css)
- Map price: $97 → $149 → $97 (held at $97 retail)
- Custom build restructured: $7K → $15K retail, with Y1 SOS price at $7.5K (50% off)
- SOS college data integration folded into Y1 custom build
- Coordinator support reduced to $0 (included in package)
- Research partnership reduced from $15K to $5K; the $10K redistributed across other lines
- Careers database expanded: 649 careers → 3,000+ careers, tasks, and leisure activities
- Section 5 restructured: DB details, SOS data, scholarships in order
- Time-savings and anti-commission-bias benefit emphasized in opening + §4 + §9
- Cover accent: orange → pale pink → pale sky blue
- Training course: "6-8 hours" → "6 hours"; marked as existing product (implicit, no over-explaining)
- Timeline: removed hard dates from "Next step" + §10
- Rate references softened: "preferred partner rate" throughout, no dollar figures for MNTEST
- Children/students added to Steven's bio line
- Paralipsis memory saved at `~/.claude/.../memory/feedback_paralipsis.md`

---

## Supporting materials

| File | What it is |
|------|------------|
| [materials/priya-sharma-map.pdf](materials/priya-sharma-map.pdf) | Sample Xavigate Map for validation profile Priya (covid-orphan, Karnataka, SOS-context) |
| [materials/sos-sample-report.pdf](materials/sos-sample-report.pdf) | Sample SOS report |
| [materials/sos-sample-report-v2.pdf](materials/sos-sample-report-v2.pdf) | Sample SOS report, v2 |
| [materials/sos-sample-report.html](materials/sos-sample-report.html) | Sample SOS report, HTML source |
| [scope/](scope/) | Per-component scope docs (older, may be partially superseded by proposal) |
| [pricing/PRICING-MODEL.md](pricing/PRICING-MODEL.md) | Earlier pricing reasoning (superseded by current proposal; kept for reference) |

---

## Superseded / outdated

| File | Status |
|------|--------|
| [proposal-2026-04-17.md](proposal-2026-04-17.md) | Original V1 draft. **Do not use.** Replaced by v2. |
| [README.md](README.md) | Pricing snapshot is outdated (shows $8/MNTEST, 80-90% Map discount, $5-10K setup). Keep for general project context but pricing is wrong. |

---

## Open decisions before sending

1. **Primary contact at SOS** — 18 institutional directors in MailerLite. Who's the right first read?
2. **Delivery pipeline for the Map PDF** — coordinator-submitted + MNI-generated, self-service on xavigate.com, or local tool? Not resolved in proposal.
3. **Currency** — proposal is USD. SOS may prefer INR invoicing.
4. **Multi-year commitment incentive** — price-locked at $20K/yr is offered; no additional discount proposed. Revisit?
5. **Webinar language** — English only, or Hindi / Tamil / Telugu available?
6. **Research MOU** — separate document to be drafted once proposal is accepted. IRB / ethics review process — who drives: MNI or SOS?

---

## Next step

Steven reviews the PDF, identifies any remaining changes, then proposal is sent to the first SOS contact.
