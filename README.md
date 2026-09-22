# Reachventory

Static, pre-launch B2B data storefront. Source assets and deployed output live in `dist/`. No build tools, database, secrets or backend are required.

## Implemented

- Homepage with three featured collections and a separate `collections.html` catalog.
- Thirty collections: 25 business lists and five aggregate consumer-market profiles.
- Recommended buyers displayed on every collection card and detail view.
- Category filters and search across industries, fields and recommended buyers.
- Accessible native dialogs for product detail, samples and project briefs.
- Three configurable proposed packages: Essential $249, Intelligence $749, Bespoke from $1,500.
- Per-collection fictional sample CSV downloads and local-only text brief generation.
- Consumer profiles use area records (25 / 100 / custom), not personal contacts. The builder supports geographic units and area median-income thresholds for income profiles.
- Responsive styling, keyboard focus treatment, reduced-motion support, metadata and favicon.
- Optional feature-detected WebMCP brief configuration.

## Commercial launch gates

This is not a functioning paid-data business yet. It deliberately does not collect payments, submit leads or pretend datasets exist. Confirm brand name and legal entity; review price economics and coverage; establish legitimate data-sourcing and redistribution permissions; create and quality-check actual lists; choose sales inbox or server-side inquiry endpoint; finalize privacy/terms/refund and rights-request procedures with appropriate advice; connect payments and secure fulfillment; then enable public access and a chosen domain. Never store payment secrets in frontend files. Do not expose paid CSVs as public static assets.

## Future integration

Catalog definitions are in `dist/app.js` and `dist/catalog-data.js`. Load catalog-data.js before app.js. Add backend order and inquiry endpoints separately. Authentication, protected download entitlements, payments webhooks and a database can be introduced when commercial fulfillment is ready. Keep server-side pricing authoritative. No contact submissions or storage happen in this version.

The consumer catalog plans aggregate Census/ACS market research only: income-based territories, homeownership, population growth, household size, and metro/neighborhood profiles. Include geographic identifiers, vintage and estimate uncertainty. Never map area median income to named individuals or use these market profiles to make individual eligibility decisions. ZCTAs are not exact postal ZIP boundaries. No consumer contact lists are implemented.

## Validation

Run `node --check dist/app.js`. Static managed preview is unavailable; desktop/mobile browser visual QA remains a launch check. WebMCP registration is feature-detected; supported live-context validation is not available in this environment.
