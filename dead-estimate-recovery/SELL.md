# Rebooked Co, Dead Quote Recovery: how to run it

The unsold-estimate sibling of the Dead List Profit Audit. Same rule, different list: bring back money the owner already paid to create. Hosted as a rebookedco.com page.

## The offer (what Hormozi would build, locked by Fable)

- The audit is FREE. It is the lead magnet. Never charge for the diagnosis.
- Collect money now: a $500 refundable deposit at pilot signing, credited 100% against recovery fees, refunded in full if the 30-day guarantee target is missed. This is the cash-today instrument, and it stays risk reversed.
- Pay per recovered job: the greater of $250 or 20% of that job's first-year value (floors $75 to $250 by trade), charged only after the job books, is serviced, and pays.
- The Follow-Up Desk: $400 a month, so no future estimate ever goes cold. Month to month.
- Guarantee: "No recovered jobs, no fee" plus the 30-day gross-profit guarantee.
- Scarcity (Alex's actual mechanic, not geographic): a client-count cap ("we take just 5 new clients a month") plus competitor-denial ("your reactivation is exclusive to you, we will not run your direct competitor's list"). The transcripts show Hormozi caps by client count and avoids geographic territory limits, so we dropped "one company per service area." The number 5 is a marketing cap you can tune (it appears in the topbar, hero eyebrow, guarantee block, final CTA, and reserve section of offer.html, plus the report closing block). Lower equals more urgency, so set it to whatever you can honestly fulfill.
- Setup fee ($300) lives inside the pilot agreement post-proof, not on the page.

## Files

- `offer.html`: the rebookedco.com landing page. Free-audit CTA plus a $500 deposit checkout (Stripe and PayPal). Interactive dead-quote calculator at the cited 10% rate. Demand-proof band with source links.
- `audit-report.html`: the fillable deliverable (tokens). `audit-report-SAMPLE.html` and `.pdf`: a filled plumbing example ($8,840 recoverable).
- `DEMAND-EVIDENCE.md`: every cited stat with its source.
- `COPY-SPEC.md`: Fable's locked copy and pricing (source of truth).
- `CODEX-REVIEW.md`: the adversarial pass and fixes.

## Go live (5 minutes)

1. Open `offer.html`, find the CONFIG block at the bottom of the file, and set three values. `AUDIT_URL` is where the free-audit button goes (a booking link, a form, or the default mailto). `STRIPE_LINK` is your Stripe Payment Link for the $500 deposit. `PAYPAL_ME` is your PayPal.Me handle, and the deposit button builds `paypalme/HANDLE/500USD`.
2. Deploy under the Rebooked site so it serves at rebookedco.com/dead-estimate-recovery (or a path you pick). Fastest test: drag `offer.html` onto Netlify Drop for an instant URL.
3. Confirm the free-audit button opens your intake, and the two deposit buttons hit Stripe and PayPal for $500.

## The sell motion

1. Pick one trade, one metro. Independents who answer their own phone. Skip franchises.
2. Opener leads with their leaked money, never the tech: "How much revenue did you write off last year in estimates that never closed? I will show you the exact number free, from your own records."
3. They reply, send the `offer.html` link. The calculator does the selling: two sliders, their own number counts up, the free-audit button is right there.
4. They request the audit. Ask for one CSV export of unsold estimates.
5. Fill `audit-report.html`, render to PDF (open in Edge, Ctrl+P, Save as PDF), deliver within 24 hours.
6. The report closes on the ladder: free audit, then the $500 deposit to start the pilot, then pay-on-result, then the $400 a month desk.

## Compliance note

Follow-ups go out from the owner, to people who requested an estimate from that owner, with the owner approving every message. No automated platform blasts the list. Opt-out is honored immediately and permanently, and a suppression list is kept across campaigns. This lowers exposure but is not a legal safe harbor: TCPA consent and revocation rules still apply to any marketing outreach, so the owner confirms consent, owns the list, and approves final copy. Do not claim "no legal risk." When automated sending is added later, it graduates to a registered A2P platform. Have the message SOP reviewed by counsel before volume.

## Before you host (from Codex review)

1. Set the guarantee mechanics in the pilot agreement (RC-PA-01) before taking any deposit: the 30-day window, which quotes count, the attribution rule, the gross-profit formula, reporting proof, refund timing, and how processor fees are treated. The page intentionally points to the pilot agreement for exact terms.
2. Attach the existing Rebooked docs: pilot agreement (RC-PA-01), SMS consent attestation (RC-CA-01), customer export checklist (RC-EX-01).
3. Replace the default `mailto:` AUDIT_URL with a real intake form and a thank-you page, and add basic conversion tracking.
4. Live-test both deposit buttons (Stripe and PayPal) for $500 before you send the link to a lead.
5. Add a short terms and privacy link in the footer.

## Fit with the rest of Rebooked

This is a distinct offer, not a replacement. The Dead List Profit Audit revives lapsed CUSTOMERS. Dead Quote Recovery chases unsold ESTIMATES. Same brand, same engine, same guarantee shape, two entry points.
