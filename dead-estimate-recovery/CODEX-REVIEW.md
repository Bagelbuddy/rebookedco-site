# Codex adversarial review: Rebooked Co Dead Quote Recovery page

Run: 2026-07-12 · codex-cli 0.136.0 · piped offer.html + audit-report-SAMPLE.html + SELL.md + DEMAND-EVIDENCE.md.

## Findings and disposition

| Sev | Finding | Disposition |
|---|---|---|
| BLOCKER | Deposit path not live (STRIPE_LINK and PAYPAL_ME empty) | By design. DK sets both in the config, then live-tests. Page shows a setup warning until set. Documented in SELL.md. |
| BLOCKER | 30-day gross-profit guarantee undefined (gross profit, attribution, window, refund timing) | Page now points to the pilot agreement for exact terms. Defining RC-PA-01 mechanics is step 1 of the "Before you host" checklist in SELL.md. DK owns the legal definition before taking a deposit. |
| HIGH | TCPA/A2P framing too casual ("outside A2P territory") | FIXED in SELL.md: removed the safe-harbor confidence, added consent, opt-out logging, suppression, counsel-reviewed SOP, and "do not claim no legal risk." |
| HIGH | PayPal deep-link fragile | FIXED: switched to `paypal.me/HANDLE/500USD` and the handle is sanitized (strips URL, @, and trailing path). |
| HIGH | Calculator label overstated ("sitting in your dead quotes" was the recovered slice, not the pool) | FIXED: label now reads "Recoverable from your dead quotes this year, at a 10% rate." |
| HIGH | 10% sold as "middle/honest" (middle of 5% to 12% is 8.5%) | FIXED on page and report: reworded to "we plan at 10%, inside the published range." Dropped "middle" and "honest." |
| HIGH | Evidence reads stronger than the sources support | FIXED: added "reported by third-party industry sources" note above the proof band, and an honesty note in DEMAND-EVIDENCE.md clarifying the PHCC stat is cited by US Tech, not linked directly. |
| MED | Pricing contradiction ("greater of $250 or 20%" vs "floors $75 to $250") | FIXED on page and FAQ: "the greater of your trade's floor (from $75, and $250 for plumbing and HVAC) or 20%." |
| MED | Sample "18 months" used gross revenue, ignoring COGS and the fee | FIXED: reworded to "the gross revenue from one recovered job covers 18 months of the $400 desk." |
| MED | Missing host-to-sell basics (terms, privacy, intake, thank-you, tracking) | Added to the "Before you host" checklist in SELL.md. DK task, not code. |

Sample math verified by Codex: 84 minus 16 equals 68, 68 times $1,300 equals $88,400, times 10% equals $8,840. Consistent.

## Codex's single highest-priority fix
> "Do not host the deposit CTA until the pilot agreement defines the guarantee and refund mechanics, and the Stripe and PayPal links are live-tested."

Both are on DK: define RC-PA-01 guarantee terms, set and test the payment links. Everything else is fixed in the files.

## Still on DK (not code)
1. Define the guarantee and refund mechanics in the pilot agreement (RC-PA-01).
2. Set STRIPE_LINK and PAYPAL_ME, live-test both at $500.
3. Real intake form and thank-you page in place of the default mailto.
4. Terms and privacy links in the footer.
