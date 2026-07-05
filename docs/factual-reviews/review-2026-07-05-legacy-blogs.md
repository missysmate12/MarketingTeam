# Factual & Compliance Review — Legacy Blog Library (blog-01 to blog-05)
**Reviewer:** Marketing Review Agent
**Date:** 5 July 2026
**Scope:** The 5 blogs in `blogs/` carrying a `Status: Awaiting Review` header (`blog-01` through `blog-05`). Despite `content-plan-2026-W27.md` referring to these as "5 published blogs," none had actually been through the factual/compliance review already applied to `nda_blog_debt_review_2026.md` and `nda_blog_rate_hike_2026.md` (see `f7f27af`). This review closes that gap.

---

## Why this review happened now

The previous AI-optimization review (`docs/ai-optimization-reviews/review-2026-27.md`, 30 June 2026) flagged one open action item: fix the unverified "up to 50%" repayment claim in `blog-05-surviving-2026-cost-of-living-crisis.md` before publishing. That fix had not been applied. Re-checking the full legacy library for the same pattern surfaced a second, previously undetected instance in `blog-02-7-warning-signs-you-need-debt-review.md`.

## Findings

| # | File | Claim | Verdict | Action |
|---|------|-------|---------|--------|
| 1 | `blog-05` | "Reduce your combined monthly debt repayment by up to 50%" | **Non-compliant** — unverifiable, specific outcome promise. Previously flagged, never fixed. | Corrected to qualitative language. |
| 2 | `blog-02` | "reduce their monthly repayments by up to 50%" | **Non-compliant** — same issue, not previously caught. | Corrected to qualitative language. |
| 3 | `blog-05` | "Section 189 rights ... under the Basic Conditions of Employment Act" | **Minor legal inaccuracy** — Section 189 (retrenchment consultation) is a Labour Relations Act provision, not BCEA. | Reworded to attribute each entitlement to the correct Act. |
| 4 | `blog-01`, `blog-04` | "Voted South Africa's best debt counselling company in 2020" | **Unverified** — no awarding body or source cited; appears identically in both files. | Flagged as action item (not altered — plausible but unconfirmed). |
| 5 | `blog-04` | "Most NDA clients complete debt review within 36 to 60 months" | **Unverified** — specific internal performance statistic, no source. | Flagged as action item. |
| 6 | `blog-01`, `blog-03` | NCR Debt Help System (DHS) offline Feb–Mar 2026, restored 31 March 2026 | Internally consistent across both files; no external source accessible (site returns HTTP 403 to crawlers). | Flagged for pre-publish verification against official NCR communication. |
| 7 | `blog-02`, `blog-03` | Office address "9 Long Street, Cape Town" | Internally consistent; unverifiable from this environment. | Flagged for pre-publish confirmation. |
| 8 | `blog-01` | Description of 2026 NCR reforms (stricter affordability checks, itemised fee disclosure, heightened compliance monitoring) | Directionally consistent with rest of repo; not tied to a specific Gazette notice/circular number. | Flagged — recommend citing the specific regulation before publishing, same standard applied to SARB figures in `nda_blog_rate_hike_2026.md`. |
| 9 | `blog-03`, `blog-04` | Form 19 clearance certificate, NCA asset protection, Prescription Act 3-year general period, free annual credit bureau report entitlement (TransUnion/Experian/Compuscan/XDS) | **Verified accurate.** | None. |

## Corrections applied this pass

- `blogs/blog-02-7-warning-signs-you-need-debt-review.md` — "up to 50%" claim corrected; reviewer notes added.
- `blogs/blog-05-surviving-2026-cost-of-living-crisis.md` — "up to 50%" claim corrected; Section 189/BCEA wording corrected; reviewer notes added.
- `blogs/blog-01-ncr-2026-changes-what-you-need-to-know.md` — no text changes; action items documented in reviewer notes.
- `blogs/blog-03-life-after-debt-review-clearance-certificate.md` — no corrections needed; verification noted.
- `blogs/blog-04-debt-review-myths-debunked.md` — no text changes; action items documented in reviewer notes.

All five files keep their `Status: Awaiting Review` header — this review covers factual/compliance accuracy only. Final client sign-off is still required, consistent with the two-step workflow in `.claude/agents/marketing-content.md`.

## Recommendation for next review cycle

The "up to 50% repayment reduction" phrasing has now appeared in **three** separate blogs (`nda_blog_debt_review_2026.md`, `blog-02`, `blog-05`) despite being corrected once already. Recommend a repo-wide grep for `up to \d+%` as a standing pre-publish check, since this is a recurring, easy-to-reintroduce compliance risk rather than a one-off error.

---

## Addendum — 5 New Drafts from the Overdue Week 27 Content Plan

`content-plan-2026-W27.md` (prepared 30 June 2026) prioritised 5 content ideas with publish targets between 1–18 July 2026. As of this review (5 July 2026), none had been drafted — item #3 (two-pot) was due today. All 5 were drafted this session and fact-checked against only the figures already verified in the content plan:

| Priority | File | Verified figures used | Fact-check result |
|---|---|---|---|
| 1 | `nda_blog_july_cost_shocks_2026.md` | 9.01% electricity increase (1 Jul 2026), repo 7%/prime 10.5% (28 May 2026), petrol R28.06/L | **Pass.** Illustrative household maths verified by hand: 9.01% of R1,500 = R135.15 ✓; 60L/week at R28.06 × 52 ÷ 12 ≈ R7,296/month (article rounds to ~R7,290, negligible rounding, both labelled "roughly") ✓; R168/R1m bond figure matches the verified figure already in `nda_blog_rate_hike_2026.md` ✓. All example figures explicitly labelled illustrative, no outcomes guaranteed. |
| 2 | `nda_blog_high_earners_debt_2026.md` | DebtBusters Q1 2026: 303% debt-to-income, 101% of take-home pay (R50k+/month earners) | **Pass.** Only the two supplied figures used, both attributed to DebtBusters as third-party reported data, not NDA's own claim. No other statistics invented. Reviewer notes correctly flag confirming the exact DebtBusters figures against the published report before going live. |
| 3 | `nda_blog_two_pot_debt_2026.md` | Two-pot: R57bn/4m transactions; DebtBusters: 64% of income to debt | **Pass.** Only the two supplied figures used, both qualified as "reported." Before/after example explicitly labelled illustrative/hypothetical. Reviewer notes correctly flag reconfirming both figures close to publish date. |
| 4 | `nda_checklist_july_squeeze_2026.md` | 9% electricity, prime 10.5%, petrol ~R28/L, 40% affordability threshold | **Pass.** Figures match the content plan brief exactly; format (email + carousel) fills the genuine format gap the plan identified; no new statistics introduced. |
| 5 | `nda_blog_mpc_july_preview_2026.md` | 23 Jul 2026 MPC date; confirmed 28 May 2026 hike (repo 7%/prime 10.5%) | **Pass.** Correctly frames a further hike as speculative only ("if," "analysts are watching") — never asserts one as fact. No invented CPI/oil/analyst figures. Reviewer notes flag reconfirming the MPC date and checking whether a decision has actually been announced by publish time. |

All 5 remain in `PENDING REVIEW` status pending final client sign-off, consistent with the repo's two-step workflow. No factual or compliance corrections were needed to any of the 5 drafts.

### Priority ranking carried forward from the content plan, with reasoning

1. **July cost-shocks blog** — highest priority: three simultaneous, already-landed cost shocks (electricity, prime, petrol) are the strongest, most time-sensitive search-intent trigger, and the publish window (1 July) has already passed, making this the most overdue.
2. **High-earners debt blog** — second priority: a genuinely new, counter-intuitive audience segment (backed by third-party data) that expands NDA's addressable market; no urgency tied to a specific date, but the content gap is real and undiluted by time.
3. **Two-pot withdrawal blog** — third priority: ties two live, high-search topics (two-pot access and debt) together; due today (5 July) per the plan, so it is now the most time-overdue item after #1.
4. **July squeeze checklist** — fourth priority: reuses the same verified figures as #1 in a lower-effort, higher-shareability format (email/social); valuable but redundant with #1's core facts, so it can follow rather than lead.
5. **MPC July preview** — fifth priority: correctly time-gated to the 23 July 2026 meeting, so it has the most runway before it goes stale; also carries the most risk of going out of date if a decision is announced early, so it should be re-verified closest to its actual publish date.
