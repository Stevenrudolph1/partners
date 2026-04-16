# SOS Partnership — Pricing Model (INTERNAL)

**Status:** Draft for Steven's review before proposal goes out.
**Currency:** USD throughout (SOS India is an institutional client paying in USD historically).
**Principle:** Considerate of nonprofit mission, but preserves MNI unit economics. Volume discounts tied to commitment, not to nonprofit status alone.

---

## 1. Inputs and Constraints

### What we already know

| Fact | Source |
|------|--------|
| SOS has used MNTEST since 2012 | partners/ legacy, contacts.md |
| Current MNTEST rate to SOS | ~$8/student |
| Most recent tranche | 700+ MNTESTs |
| 18 director contacts in MailerLite | contacts.md `institutional` group |
| Xavigate Map retail | $97/person |
| Xavigate training course retail | $599/seat |
| College matcher (SOS edition) | Already built — program-matcher-india |
| Custom report template | Already built — generate_sos_pdf.py, 9 sections |
| Custom intake form | Already built — 7-tab wizard |

### What Steven specified

- MNTEST stays at $8 (don't disrupt).
- Xavigate Map: 80-90% volume discount against $97 retail.
- Training course: $599 retail, similar volume discounts.
- Customization fee for intake + report.

### What constrains pricing

- Unit cost floor: server, support, bandwidth, Shriya fulfillment time, email system.
- Mithya Labs (Saurabh) profit share on paid products — commercial Xavigate Map revenue is part of that.
- 14-year relationship. Trust and continuity matter more than maximum extraction.
- SOS is a nonprofit serving orphan/at-risk children. Message discipline: mission-priced, not "charity-priced."

---

## 2. Per-Student Pricing Stack

### MNTEST — $8/student (unchanged)

- Retail context: MNTEST is ~$15-25/student for non-institutional buyers.
- SOS rate reflects 14-year relationship and bulk.
- No change proposed. Disruption risk outweighs revenue opportunity.

### Xavigate Map — SOS Edition

**Retail:** $97/person (xavigate.com).
**SOS rate:** Volume-tiered between $12 and $20.

| Annual volume | Map rate | Discount | Rationale |
|---------------|----------|----------|-----------|
| 1-499 | $20 | 79% off | Low volume floor; covers delivery infrastructure |
| 500-999 | $17 | 82% off | Mid-volume, matches recent 700+ tranche |
| 1,000-1,999 | $15 | 85% off | Volume SOS would likely commit to |
| 2,000+ | $12 | 88% off | Aspirational; full-cohort deployment |

**Why 80-90% discount is defensible:**
- Marginal cost per Map is low (server + storage + minor support). Engineering was paid for in the Phase 1-6 build.
- Retail pricing is calibrated for individual Western buyers; not a fair benchmark for institutional India pricing.
- SOS cohort is a validation and testimonial source worth more than the pricing gap.
- Mithya Labs profit share is volume-dependent; higher volume at lower rate compensates.

**Floor analysis:** Even at $12/student × 2,000 students = $24,000/year. Solid recurring revenue from a single institutional client. Not charity.

### Per-student total

| Volume tier | MNTEST | Map | Total/student | Retail equivalent |
|-------------|--------|-----|---------------|-------------------|
| 1-499 | $8 | $20 | $28 | $105+ |
| 500-999 | $8 | $17 | $25 | $105+ |
| 1,000-1,999 | $8 | $15 | **$23** | $105+ |
| 2,000+ | $8 | $12 | $20 | $105+ |

---

## 3. Training Course — Institutional Pricing

### Retail

- Individual seat: $599. No volume discount on retail channel.

### SOS institutional rates

Two tiers — avoid per-seat counting overhead. Coordinator seats are what SOS actually needs.

| Tier | Price/year | Seats | Reasoning |
|------|------------|-------|-----------|
| **Bundle** | $2,499 | Up to 25 coordinators | Enough for most SOS regional teams |
| **Unlimited** | $7,499 | All SOS coworkers in India | For full-network rollout |

**Why not per-seat:**
- Administrative overhead of seat counting isn't worth it for an institutional relationship.
- Bundle/unlimited framing signals confidence and partnership.
- At $2,499 / 25 = $100/seat — already 83% off retail — while giving SOS simple procurement.

**Unlimited math check:** If SOS has 500 coworkers in India eligible, unlimited at $7,499 = $15/seat effective, or 97% off retail. Aggressive, but defensible because course production cost is sunk once produced and marginal LMS cost is negligible.

**Annual renewal.** Not perpetual. Protects MNI.

---

## 4. One-Time Customization Fees

These exist primarily to (a) signal commitment from SOS and (b) recognize real engineering work. Can be waived when volume justifies.

| Item | Fee | Waiver condition | Real cost |
|------|-----|-------------------|-----------|
| Custom SOS intake form | $2,500 | Waived if Map volume ≥ 500/year | Already built — fee is for ongoing maintenance + minor tweaks |
| Custom SOS report template | $4,500 | Waived if Map volume ≥ 1,000/year | Already built — fee is for maintenance + updates + DB refresh work |
| Training course customization | $3,500 | Non-waivable | Real production cost (video, workbook, examples) |
| **Total outright** | **$10,500** | — | — |
| **Total if volume met** | **$3,500** | — | — |

**Steven decision point:** Should the intake + report fees be waived outright given they're already built? Argument FOR charging: signals partnership commitment, covers ongoing DB + infrastructure costs. Argument AGAINST: SOS already paid for it in 14 years of MNTEST relationship. Default is to keep them but offer the volume waiver — SOS can earn their way out.

---

## 5. Webinar Subscription

Recurring delivery of Steven's time (and/or team time). Priced to reflect that.

| Tier | Price/year | Includes |
|------|------------|----------|
| Basic | $4,800 | 4 coworker webinars + archive |
| Full | $7,200 | 4 coworker + 4 children webinars + archive |

**Per-webinar cost analysis:**
- Basic: $1,200 per webinar delivered — Steven's time + prep + platform + follow-up materials.
- Full: $900 per webinar delivered — volume discount for 8/year.

**Alternative Steven may prefer:** Per-webinar quote. If SOS prefers to book ad-hoc rather than subscribe, quote $1,500-2,000/webinar on demand. The subscription locks in MNI revenue and cadence.

**Risk:** Steven's time is finite. If SOS maxes out the subscription with demanding sessions, is $4,800-7,200/year worth the commitment? At 8 hours per webinar (prep + delivery + follow-up), that's 32-64 hours/year. Hourly implied rate: $112-150. Acceptable for institutional work given the relationship.

---

## 6. Research Partnership — In-Kind

**No cash changes hands.** Both sides contribute in-kind.

### MNI contributes
- Free MNTEST + Map assessments for study participants (up to 500/year).
- Analytical work (data cleaning, statistical analysis, manuscript drafting).
- Positioning the study for publication.

### SOS contributes
- Cohort access (historical MNTEST takers 2012-present).
- Follow-up data collection (outcomes, satisfaction, earnings).
- IRB / ethics approval (SOS likely has institutional review infrastructure).
- Co-authorship and SOS India brand endorsement.

### Valuation (hypothetical)

If priced commercially:
- 500 free assessments × $23 = $11,500/year in-kind from MNI.
- Analytical work: ~$15,000-30,000 project-equivalent.
- SOS cohort data access: significant research value, hard to price but likely comparable.

**No line item in the proposal invoice.** Separate MOU covers this track.

---

## 7. Annual Example (1,000 students)

This is the scenario the proposal uses as illustration.

| Line item | Amount |
|-----------|--------|
| MNTEST (1,000 × $8) | $8,000 |
| Xavigate Map (1,000 × $15) | $15,000 |
| Training bundle (25 coordinators) | $2,499 |
| Webinars — full tier | $7,200 |
| Customization fees | $0 (volume met) |
| Research partnership | In-kind |
| **Total** | **$32,699** |

**Per-student effective rate:** $32.70.
**Roughly half the retail price of MNTEST + Map alone ($105+).**

### Scenario A — Smaller commitment (500 students)

| Line item | Amount |
|-----------|--------|
| MNTEST (500 × $8) | $4,000 |
| Xavigate Map (500 × $17) | $8,500 |
| Training bundle | $2,499 |
| Webinars — full tier | $7,200 |
| Customization fees | $4,500 (report fee still applies at <1,000) |
| **Total** | **$26,699** |

### Scenario B — Full commitment (2,000+ students)

| Line item | Amount |
|-----------|--------|
| MNTEST (2,000 × $8) | $16,000 |
| Xavigate Map (2,000 × $12) | $24,000 |
| Training unlimited | $7,499 |
| Webinars — full tier | $7,200 |
| Customization fees | $0 (volume met) |
| **Total** | **$54,699** |
| **Per student** | **$27.35** |

---

## 8. Revenue Projections to MNI

Assuming Scenario A (500 students) as conservative and Scenario B (2,000) as aggressive, over a 3-year partnership:

| Year | Conservative (500/yr) | Moderate (1,000/yr) | Aggressive (2,000/yr) |
|------|------------------------|---------------------|------------------------|
| Year 1 | $26,699 | $32,699 | $54,699 |
| Year 2 | $22,199 (no custom fees) | $32,699 | $54,699 |
| Year 3 | $22,199 | $32,699 | $54,699 |
| **3-year total** | **$71,097** | **$98,097** | **$164,097** |

Research partnership not included. Retention track record (14 years) suggests this is durable recurring revenue.

---

## 9. Pricing Decisions to Lock Before Sending

Steven to decide:

1. **Waive customization fees entirely?** (Currently: volume-gated waiver.)
2. **Webinar format:** subscription or per-webinar?
3. **Multi-year discount?** (E.g., 5% off all prices if SOS commits to 3 years upfront.)
4. **Include print/shipped interpretation guides?** (Currently digital only — adds ~$500/year shipping budget to add print.)
5. **USD vs INR?** SOS directors may prefer INR invoices.
6. **Course customization needed?** If generic MN/Map course works, save $3,500 customization fee.

---

## 10. What This Does NOT Cover

Explicitly out of scope for this proposal:

- Individual coaching/consulting with specific students (would be ad-hoc engagement)
- White-label reports (SOS logo on MNI template — negotiable separately)
- Integration with SOS internal systems (CRM, student records)
- Custom software development beyond intake + report
- Translation into regional Indian languages (would be a separate project)
- Ongoing DB maintenance beyond the Map infrastructure

Each of the above can be a separate quote if SOS wants.

---

*Last updated: 2026-04-17*
