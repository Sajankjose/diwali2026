# Geojit Diwali 2026 — GitHub Pages package

## Publish
1. Extract this ZIP on your computer.
2. Create or open your GitHub repository.
3. Upload the extracted files into the repository root, with index.html directly at the top level. Upload the files, not the ZIP or its enclosing folder.
4. Commit the files to main.
5. Open Settings → Pages.
6. Under Build and deployment, set Source to Deploy from a branch.
7. Choose main and /(root), then Save.
8. Wait for deployment and open the URL displayed by GitHub Pages.

No npm install, build command, dist folder setting or API keys are required.
Documentation: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Included
- index.html: entry page
- style.css: responsive Diwali styling
- app.js: tap-to-advance flow, shortlist, insurance guidance, keepsake and sharing
- catalogue.js: 12 supplied stocks and 133 supplied funds
- geojit-white.png: supplied official logo
- .nojekyll: plain static hosting

All local asset references are relative and work under a repository subpath.
Sharing automatically uses the deployed page address. This export removes the ChatGPT-private-preview notice from the share dialog; it does not change the existing hosted preview's access.
Fonts use Google Fonts with local fallback fonts. Saving is optional browser-local storage. WhatsApp and email open user-controlled sharing/draft flows; no messages are sent automatically.

## Updated content
The supplied Geojit stock and fund lists are connected. Exact source records, dates, minimum amounts and footnotes are preserved. Rationale is explanatory portfolio-role reasoning, not a company research thesis supplied in the files. The gift now shows illustrative target allocations, not executable orders or approved Geojit weights. Whole-share feasibility must be checked at live prices.

## Hosting
Upload all files together, including catalogue.js. No build command or API key is needed. Sharing uses the deployed GitHub Pages address. The existing private preview remains unchanged in audience.

## Verification
Syntax, data counts, source restrictions, shortlist gates, navigation transitions and export content checked. Browser visual QA remains unverified.


## October 16 responsive portfolio update
- Form navigation is in normal document flow; no fixed bottom controls cover inputs.
- Result navigation uses accessible, keyboard-operated sticky tabs; one section is visible at a time.
- Four-sector stock basket stays visible, with equal target weights when eligible and an unallocated watchlist otherwise.
- Separate lump-sum and SIP budgets reconcile independently. Fund selection uses supplied ratings then sheet order; lump-sum minima and restrictions are respected. SIP minima remain unverified.
- Insurance shows concise priorities with expandable personal context and next steps.
- Downloaded keepsakes include allocations and guidance; shared invitations exclude personal answers.

### Illustrative model rules
Foundation/unknown/minor profiles remain unallocated. Near-term or cautious profiles use debt categories only. Other profiles target 25% equity funds at 3–5 years, 45% at 5–7 years, and 50% (60% with high willingness and capacity) at 7+ years. Strong profiles with some stock experience and at least ₹10,000 may target 10% stocks at 5–7 years or 20% at 7+ years. Remainder goes to debt categories. These are application assumptions, not approved research weights. SIP splits renormalize the fund weights and exclude stocks. No live-price order quantities are produced.
General allocation principles: https://investor.sebi.gov.in/investment-thingsbeforeinv.html (does not endorse these weights).

### Validation
Run `node test-portfolio.cjs`: 900 budget/profile combinations check independent budget reconciliation, minimums, restrictions, sector mix and risk gates. DOM-stub checks cover flow rendering and export. `node --check app.js` passes. Physical-device / browser visual QA is not completed; responsive CSS was reviewed against the supplied iPhone overlap screenshots.
