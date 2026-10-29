# Morrow — feature-rich static PWA prototype

A mobile-first mortgage planning web app designed for an England-focused educational use case.

## Included features
- Responsive desktop side navigation and mobile bottom navigation
- Mortgage setup: balance, current rate, monthly repayment, remaining term, estimated property value and optional deal-end month
- LTV goals (80%, 75%, 70%, 65%, 60% and 59.5%), monthly overpayment and one-off lump sum
- Overview dashboard, progress/milestone estimate and SVG balance comparison chart
- What-if tools for monthly extras, lump sums and ±5%/±10% valuation cases
- Year-by-year balance and LTV timeline, CSV export, print/save-to-PDF
- Plain-English education on LTV, overpayments and rate-deal end dates
- Download/restore JSON backup and delete locally saved plan
- PWA manifest, icon and static asset service worker for install/offline shell
- Starter privacy notes, terms and commercial strategy

## Preview locally
Open `index.html` in a modern browser. PWA installation and service-worker offline testing need HTTPS or localhost; double-clicking the HTML file will not enable those capabilities.

## Deployment recommendation
Keep the repository on GitHub for source control. For a public app that may be monetised, deploy the static files to Cloudflare Pages or another host whose terms permit the intended commercial activity. GitHub's Pages terms say its free Pages service is not intended for hosting an online business or commercial SaaS. The current provider terms and free-plan limits should be re-checked before launch.

### Publish to Cloudflare Pages
1. Create a Cloudflare account and choose **Workers & Pages → Create → Pages → Connect to Git**.
2. Select the GitHub repository.
3. For this plain static app, leave the build command empty/no build and set the output directory to the repository root (`.`) as the current UI requests.
4. Deploy, then test the HTTPS URL on desktop, Android Chrome and iOS Safari.
5. Add a custom domain later if desired; domain registration is normally a separate cost even when static hosting is free.

## Important limitations
- Prototype only; calculations have not had independent financial validation.
- The model assumes steady monthly interest, rate, payment and term. It treats an entered lump sum as reducing principal at the start. Real lenders may accrue interest daily, use different dates/rounding, apply overpayments differently, charge fees or cap overpayments.
- This is an educational illustration, not personal financial advice, a live rate comparison service or a recommendation to enter or vary a mortgage.
- No backend, account, cloud sync, reminder notifications, lender integration or live data is present.
- Local browser storage is not a secure account vault. Other people with access to an unlocked device/browser may be able to access the saved plan.
- Privacy and terms pages are starter drafts, not legal advice. Add the operator's legal identity/contact details and have the notices reviewed before public launch.
- Google Fonts are loaded externally; remove the `@import` at the top of `styles.css` for a stricter offline/no-third-party-request build.

## Production test checklist
- Test on current Chrome/Android and Safari/iOS at small and large screen sizes.
- Check zero rate, payment not covering interest, balance already below LTV target, large lump sum, early payoff, long term and decimal inputs.
- Compare calculations against independently computed amortisation cases and, where appropriate, lender illustrations.
- Test CSV and JSON export/import, deletion, offline refresh, installation and browser data clearing.
- Test keyboard-only navigation, contrast and screen reader use.
- Obtain specialist review before adding mortgage referrals, paid financial promotions or lead capture.
