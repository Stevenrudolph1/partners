# Scope — Xavigate Map, SOS Edition

**Status:** Core infrastructure built. Needs packaging, delivery pipeline, and sign-off.
**Primary build location:** [diagnostics/program-matcher-india/](../../../diagnostics/program-matcher-india/)

---

## What's Already Built

### Custom intake form
- File: `diagnostics/program-matcher-india/intake/sos_intake_form.html`
- Format: 7-tab wizard using SR design system
- Tabs: Student · Documents · Academic · Financial · Location · Natures × MIs · Review
- Captures: SOS village, care stage, documentation status (Aadhaar, caste cert, domicile, orphan cert), academic history, financial context, entrance exams, career preferences, Nature × MI scores, chosen careers
- Output: JSON matching `sos_intake_schema.json`, ready for match_v2.py

### College matcher
- File: `diagnostics/program-matcher-india/match_v2.py`
- Database: 36,000+ institutions, 126,000+ programs, 9,400+ NIRF rankings, 7,300+ placement records, 5,900+ accreditations (growing toward ~45K institutions)
- 6-gate viability filter:
  1. Documentation — student can be admitted (caste cert, domicile for state quota)
  2. Financial — SOS + scholarships cover total cost (≤ ₹1L/yr; ≤ ₹2L if PM CARES eligible)
  3. Hostel — residential option available
  4. Placement — >50% rate OR NIRF top 200 OR unknown (flagged)
  5. Location — relocation willingness vs. college location
  6. Academic — student meets admission criteria
- Nature × MI scoring applied only to colleges passing all 6 gates
- Composite quality score: NIRF + placement rate + salary + NAAC + user rating
- Dual-mode program matching (AICTE exact + non-AICTE name/LIKE for medical/law/education)

### PDF report generator
- File: `diagnostics/program-matcher-india/generate_sos_pdf.py`
- Uses shared `pdf_base.BasePDF` (same class as Xavigate Map PDF + Career Brief)
- Output: 14-page PDF, SR design system compliant
- Sections (0-8 + About):
  - 0. How to Read This Report — orientation for coordinator
  - 1. Intake Summary — verbatim verification
  - 2. Student Profile — MN + MI bar charts, constraints, cluster fit
  - 3. Career Shortlist — student's chosen careers (primary) + system shortlist (reference)
  - 4. Documentation Status — in-hand / missing critical / missing supporting / action items
  - 5. Financial Plan — per-college fee × PM CARES × SOS × gap table
  - 6. Recommendations — full college cards with NIRF/NAAC/placement/salary
  - 7. Backup Options — runner-up college table
  - 8. SOS Coordinator Checklist — 7-item numbered action list
  - About — methodology + data sources + trademarks

### HTML report generator
- File: `diagnostics/program-matcher-india/generate_report.py`
- Browser-renderable, Cmd+P to PDF
- Same 9 sections, SR Design System tokens
- Used for previewing before PDF export

### Validated end-to-end
Sample profile: Priya (age 18, orphan, Karnataka, financial pressure very_high, picks Registered Nurse / Physiotherapist / Public Health Worker).
Running: `python3 generate_sos_pdf.py intake/sample_sos_intake.json --sos --state Karnataka --output ~/Desktop/sos-sample-report.pdf`
Produces: 14-page PDF with AIIMS Bangalore as top medical match (NIRF #2, 96% placed, ₹14.9L avg salary).

---

## What's Still Needed Before SOS Can Use It

### Delivery pipeline (not yet decided)

Three possibilities — Steven to choose:

1. **Coordinator-submitted intake, MNI-generated report.** Coordinator fills intake form, emails JSON to MNI, MNI generates PDF, emails back. Manual but simple.
2. **Self-service via xavigate.com.** SOS-specific login at xavigate.com/sos. Coordinator fills form, PDF generates automatically, downloadable from account. Requires hosting + auth + deployment.
3. **Local tool for coordinators.** Ship intake form + generator as a local executable or web app SOS can run. Offline-capable. No MNI infrastructure dependency but harder to update.

Current state: only option 1 works immediately (scripts run locally on M4). Options 2 and 3 require engineering.

### Production deployment
- Decide: host at xavigate.com or ship locally?
- If hosted: subdomain? authentication model? rate limiting?
- If shipped: package for macOS/Windows? Python dependency management for non-devs?

### Phase 2 scrape completion
- 29,376 URLs still pending fetch
- 42,283 extractions still pending
- Expected final state: ~45K institutions
- Rerun `import_nirf.py` + `import_ugc.py` after Phase 2 completes to link new institutions to rankings/accreditations

### Program-map review
- 24 Nature × MI clusters currently marked "DRAFT — needs Steven review" in `mappings/program-map.json`
- Careers list (5-7 per cluster) also unreviewed
- Steven should validate before SOS reports go to real students

### Client privacy enforcement
- Steven's CLAUDE.md rule: no real client data in public-facing artifacts
- All sample/demo artifacts use fictional profiles (Elena, James, Shriya, Marcus, Priya)
- When real SOS students go through pipeline: add their names to `diagnostics/config/real-clients.txt` IMMEDIATELY
- Gate: `diagnostics/gates/client-privacy-gate.sh --site` before any artifact deploys

### Phase 4 registry expansion (optional but high-impact)
- BCI (Bar Council) — law colleges
- NMC (National Medical Commission) — medical colleges
- NCTE (National Council for Teacher Education) — education colleges
- Scholarships database — PM CARES, National Scholarship Portal, state schemes
- Impact: fills gaps in non-AICTE college data, enriches scholarship matching

### Phase 5 deep crawl (optional)
- Individual college website crawls for hostel fees, orphan quotas, exact admission criteria
- Data no aggregator has
- All LLM extraction via Claude Code on Max — no API cost

---

## What Makes This Different from Retail Xavigate Map

| Aspect | Retail Xavigate Map | SOS Edition |
|--------|---------------------|-------------|
| Intake | Generic personal + career questions | SOS-specific: care stage, documentation, financial, state |
| Report target | Individual adult | Coordinator + student |
| Career recommendations | Generic MN × MI cluster output | Student's chosen careers first, then system shortlist |
| College matching | Not included | 36K+ Indian colleges with 6-gate viability |
| Financial plan | Not included | Per-college fee × PM CARES × SOS funding × gap analysis |
| Documentation check | Not included | Full SOS documentation status + action items |
| Coordinator checklist | Not included | 7-item numbered action list |
| Data sources | Assessment only | Assessment + AICTE + NIRF + NAAC + UGC + Careers360 + CollegeSearch |

The SOS edition is effectively a different product that happens to share the MN/MI diagnostic engine with the retail Map.

---

## Pricing Implications

See [pricing/PRICING-MODEL.md](../pricing/PRICING-MODEL.md).

- Retail Xavigate Map: $97/person
- SOS Edition: $12-20/student depending on volume (79-88% off retail)
- Customization fee for intake + report template: $7,000 one-time (waivable at 1,000+/year volume)

---

## Dependencies

- Phase 2 scrape completion (in progress)
- Program-map Steven review
- Delivery pipeline decision
- Deployment decision
- SOS primary contact confirmation

---

*Last updated: 2026-04-17*
