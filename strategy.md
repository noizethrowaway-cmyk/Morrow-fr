# Morrow — simple monetisation strategy (England-only launch)

**Prepared:** 29 October 2026. This is a planning document, not legal or financial-regulatory advice.

## Positioning
Position Morrow as a free, privacy-conscious mortgage clarity tool for homeowners in England. It helps people understand their current balance, model repayment scenarios and keep track of an LTV goal. It does **not** tell people which mortgage to take or claim a target LTV guarantees a better deal.

## Revenue model: earn trust before offers

### Phase 0 — Validate the product (weeks 1–4)
- Host the static PWA on Cloudflare Pages Free or a comparable host whose current terms permit the intended use. Keep GitHub for source control rather than assuming GitHub Pages is the right permanent host for a commercial service.
- Keep the core calculator free. No behavioural advertising or paid lead capture.
- Run 10–20 mobile usability tests with England-based homeowners. Check whether people complete setup and correctly explain LTV in their own words.
- Start with qualitative feedback. Add analytics only after reviewing PECR/UK GDPR implications and consent.

### Phase 1 — First small commercial test (months 2–3)
Prefer **clearly labelled non-financial homeownership partner placements**: for example, home-energy assessments, conveyancing information, surveyors or home-maintenance services. Validate partners, terms and audience fit. Keep placements small, relevant, optional and visually separate from mortgage calculations. Do not imply endorsement or “best in market”.

A second option is a **sponsored educational guide** from a relevant homeownership provider. Mark it “Sponsored” clearly at the heading and identify who paid. Keep the sponsor from influencing the tool's calculation results.

Avoid display-ad networks early: they can create tracking overhead, distract users and weaken the privacy promise.

### Phase 2 — Mortgage referrals only after specialist review
Mortgage referrals may be relevant commercially, but have the highest regulatory risk. Do **not** launch mortgage lead forms, personalised recommendations, “best deal for you” rankings, prefilled broker hand-offs or paid introductions until a UK financial-services regulatory specialist reviews the exact journey and remuneration model in writing.

Safer exploration path:
1. Talk to an FCA-authorised mortgage intermediary or network with compliance support.
2. Show the exact screens, copy, collected fields, referral journey, remuneration terms and marketing plan.
3. Obtain a documented perimeter/compliance review. Confirm whether Morrow's role needs FCA permission, may operate within a compliant arrangement, or must remain general-information publishing.
4. Obtain compliance-approved promotions and wording before publishing mortgage-related promotions.
5. Give users an explicit choice to leave Morrow and contact the named authorised firm. Disclose paid relationships beside the link. Do not share mortgage figures or contact details without a separate, informed choice and an appropriate privacy notice.
6. Record approvals, partner status checks, published versions and complaints.

A disclaimer alone does not make a regulated activity or financial promotion lawful. The FCA perimeter is fact-specific.

## Simple illustrative revenue model

This is a sensitivity exercise, **not a forecast or a promised commission rate**. At 10,000 monthly active visitors:
- 1% click a clearly marked partner placement = 100 clicks.
- 5% of clicks complete a tracked outcome = 5 outcomes.
- If a hypothetical partner payment were £40 per outcome, that would be £200/month before costs, tax, refunds or tracking failure.

Real performance and partner terms could be much lower or higher. Validate actual terms first. A fixed, disclosed monthly sponsorship may be easier to model than affiliate outcome fees.

## Product rules for monetisation
- Keep the core tool free and usable without giving contact details.
- Never sell or share the user's mortgage balance, property value or scenarios.
- Never rank a partner higher because it pays more.
- Label commercial placements “Advertisement” or “Sponsored”; for affiliate links, disclose that Morrow may receive payment.
- Avoid claims such as “guaranteed best rate”, “you will save £X”, “you qualify” or “this lender is best for you”.
- Keep offers optional and outside calculation outputs.
- No pre-ticked consent boxes or bundled marketing permission.
- Add a complaints/contact route and a way to report a misleading or broken partner link.

## England-only scope
- Say “for homeowners in England” where appropriate in launch copy, service coverage and partner listings.
- Do not claim that residence is verified. A static app cannot reliably establish a user's location or eligibility.
- Important aspects of mortgage regulation operate across the UK; England-only marketing does not remove FCA requirements.
- Use English property/mortgage terminology. Avoid Scotland-, Wales- or Northern Ireland-specific legal/housing processes unless separately reviewed.
- Do not add tax or legal calculators (such as stamp duty) until current rules are maintained and reviewed.

## Trust, privacy and operations checklist
Before commercial launch:
- Publish operator legal identity/contact details, complete privacy notice, terms, complaint/contact route and effective dates.
- Review whether UK GDPR applies to data collected and whether the ICO data protection fee is payable or an exemption applies.
- Document data flows, vendors, retention and deletion. Hosting providers may log technical data even when the mortgage figures stay on-device.
- Obtain consent before non-essential cookies or similar tracking technologies are set or read. Avoid analytics and ad trackers until consent controls are ready.
- If using email reminders/newsletters, obtain separate clear permission and make unsubscribe straightforward.
- Keep partner due-diligence, contracts, approved copy and disclosure records.
- Seek advice on advertising/consumer-law duties, business and tax records, and VAT as turnover grows.

## Scorecard
Track only what is necessary and lawful:
1. Landing-to-setup start rate
2. Setup completion rate
3. Scenario-tool usage
4. Return visits within 30 days (using privacy-compliant measurement)
5. User-reported clarity and trust
6. Accessibility issues and calculation error reports
7. Partner click-outs and complaints, separate from any advice outcome

## Go/no-go gates
**A — Usability:** at least 80% of test users complete setup unaided; users can explain LTV; no critical mobile accessibility defects.

**B — Calculation safety:** independent tests cover zero/low interest, payments barely covering interest, overpayments, lump sums, rounding, long terms and early payoff.

**C — Compliance:** review privacy/terms and hosting; get the exact mortgage-referral model assessed before lead generation; obtain approval for any promotion where required.

**D — Commercial:** one sponsor/non-mortgage partner agrees to a small pilot with written terms and transparent measurement. Expand only when the placement helps users and feedback remains positive.

## Source links to review
- FCA, financial promotions and adverts: https://www.fca.org.uk/firms/financial-promotions-adverts
- FCA, social media financial promotions guidance: https://www.fca.org.uk/publications/finalised-guidance/fg24-1-finalised-guidance-financial-promotions-social-media
- FCA Handbook, PERG 4 mortgages perimeter: https://handbook.fca.org.uk/handbook/perg4
- ICO, cookies and similar technologies: https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guide-to-pecr/cookies-and-similar-technologies/
- ASA, affiliate advertising: https://www.asa.org.uk/advice-online/recognising-ads-social-media.html
- ICO, data protection fee: https://ico.org.uk/for-organisations/advice-for-small-organisations/getting-started-with-gdpr/data-protection-fee-what-you-need-to-know/
