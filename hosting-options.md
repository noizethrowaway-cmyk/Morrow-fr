# Morrow hosting options for a free mobile web app

Checked against provider documentation on 29 October 2026. Free plans and terms can change; re-check before deployment.

## Recommended: Cloudflare Pages Free

**Best fit for the first public demo and a future small commercial static PWA.** The current Pages documentation says static asset requests are free and unlimited on Free and paid plans, while Functions are charged/limited as Workers usage. The Free plan documentation lists up to 500 builds per month and one concurrent build. The app as built is static, so it does not need a server or a database.

Pros:
- Connects to a Git repository and deploys automatically after commits.
- HTTPS, custom-domain support and CDN delivery.
- Static hosting works well with `manifest.json` and `sw.js`.
- Leaves room to add small serverless features later, although doing so introduces quotas and more operational complexity.

Trade-offs:
- You still need to manage the domain separately if you buy one.
- A static host does not provide user accounts, cloud sync, secure data storage or backend reminders by itself.
- Understand any Cloudflare services enabled beyond static Pages, the relevant terms and applicable privacy disclosures.

Simple setup: create a Cloudflare account → Workers & Pages → Create → Pages → connect GitHub → choose the repository → use no build command and the repository root as the output directory → deploy. Confirm the UI's root-directory syntax in the current setup screen.

Official docs: https://developers.cloudflare.com/pages/ and https://developers.cloudflare.com/pages/platform/limits/

## Alternative: Netlify Free

Netlify's current pricing page offers a $0 Free plan with custom domains/SSL and a stated 300-credit monthly allowance. Its documentation says the Free plan has a hard limit and no automatic recharge. It is friendly for straightforward static deployments and preview builds.

Pros: easy Git integration, HTTPS, previews and custom-domain support.

Trade-offs: understand the credits model and what actions consume credits before relying on it for traffic. Re-check the current pricing page, including any commercial-use and fair-use terms, before launch.

Official docs: https://www.netlify.com/pricing/ and https://docs.netlify.com/manage/accounts-and-billing/billing/billing-for-credit-based-plans/credit-based-pricing-plans/

## GitHub Pages Free

Best for the source-code repository, development previews, portfolio/demo versions and non-commercial project documentation. It deploys HTML/CSS/JavaScript from a repository and supports HTTPS/custom domains.

**Important for Morrow:** GitHub says Pages is not intended or allowed as free hosting for an online business, e-commerce site or website primarily directed at commercial transactions or commercial SaaS. So do not rely on GitHub Pages as the permanent host for monetised Morrow. Keep the code on GitHub and deploy from that repository to a suitable host instead.

Official docs: https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages and https://docs.github.com/en/site-policy/github-terms/github-terms-for-additional-products-and-features

## Vercel Hobby

Vercel Hobby has a useful free developer experience, but the current terms describe Hobby as for personal, non-commercial use. It is therefore not the recommended plan for a monetised Morrow service. Vercel's paid plans may be an option later if its features suit your architecture and budget.

Official docs: https://vercel.com/docs/plans/hobby

## What costs money even when hosting is free?

You may still pay for a custom domain, legal/regulatory advice, privacy/cookie tooling, a transactional email provider, support, independent calculation testing, and any paid partner/compliance costs. A free static host does not solve privacy, financial-promotion or mortgage-regulation obligations.

## Mobile app / PWA notes

Morrow includes a Web App Manifest, icon and service worker. That gives browsers the ingredients for an installable progressive web app (PWA), not a native iOS/Android app-store listing. It is served as a website and may be added to the home screen. On iPhone/iPad, use Safari's Share menu and **Add to Home Screen**; on compatible Android browsers, use the browser's Install/Add to Home Screen option. The app currently has no backend, cloud sync, push reminders or user accounts.

## Move later without a rebuild

Keep the app static and avoid provider-specific database/auth features until there is a clear need. Put source in GitHub; configure Cloudflare Pages or Netlify to build from the repository root; point the domain DNS to the selected host; test HTTPS, install, offline refresh, data import/export and links. Keep exported mortgage backups private. Before launch, test on real iOS and Android devices.
