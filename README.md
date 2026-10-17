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


## Planning dashboard update
The discovery form asks for a comfortable monthly contribution. SIP is explained only when the fund plan is shown. Overview includes actual model percentages (after integer share rounding), a doughnut and a separate monthly budget.

### Stock construction
Within the target stock budget, cap each of four positions at 25%. Screen supplied names for affordability at undated source prices, retain source order and select four distinct business groups (Banking/NBFC grouped). Floor quantities to whole shares. If four names cannot fit, allocate zero stocks and move the unused portion into the selected debt fund when its minimum is met. Unused upfront allocations are added to the selected debt fund when its minimum is met; otherwise they remain unallocated. This is a reference-price simulation, not a live quote or order; fees/taxes are excluded. Price does not imply quality. Approved research/suitability and current prices remain necessary.

### Goal calculation
Effective monthly rate = (1 + annual rate)^(1/12) - 1. Contributions are made at month-end. Assigned investments compound at the scenario rate; unallocated balances and contributions earn 0%. The goal cost compounds at the entered inflation rate. Required monthly contribution uses the same invested/cash ratio. The crossing date searches month by month up to 50 years against the then-inflated goal, rather than a fixed future target. Sliders are scenario assumptions; only the explicit apply button changes the monthly fund allocation. Returns are not predicted or guaranteed. General calculator reference: https://investor.sebi.gov.in/calculators/sip_calculator.html

### Protection calculation
All six family-support inputs must be known. Sum annual expenses increased 5% yearly for the requested whole years, add loans/other commitments, subtract assets and current death benefits, floor the gap at zero. No investment discount is assumed. This is an expense-based planning estimate, not an underwriting decision or policy quote. Health gap compares a user-entered review target with personal cover; it does not prescribe adequate cover. Emergency runway = accessible savings / monthly family support. Unknown fields stay unknown.

### Verification
`node test-portfolio.cjs` covers 900 profile/budget combinations, whole-share quantities/caps, four-or-zero stock holdings, independent budget totals, fund restrictions, flow/exports, zero and negative return calculations and insurance arithmetic. DOM stubs do not replace visual browser/device QA; that verification remains incomplete.


## Plain-language allocation / progressive disclosure update
The default result now leads with two visible lists: upfront stock quantities and one-time fund amounts, then fund-by-fund monthly amounts. No tabs need opening to discover the allocation. Each list reconciles to its own budget and explains any unassigned amount. If no stocks fit, the first view explains the actual reason rather than only showing a zero count.

Unused stock/fund allocation amounts now go into the selected debt fund if its source minimum can be met, leaving only genuinely unallocatable amounts in reserve. This does not raise the equity target. The final doughnut uses actual allocated amounts. Monthly fund targets remain based on the original model fund weights before stock rounding.

All detailed views are progressively disclosed: allocation chart, stock rationale, fund explanations, goal scenarios and insurance guidance use closed native details elements. The overview directly explains what to do once versus every month. The monthly scenario apply action returns the user to the updated visible monthly plan. No transactions are placed.

Regression checks cover first-view holding names, quantities and monthly amounts, collapsed goal details, the no-stock reason, and redirecting a ₹10,000 example fully into funds. Existing 900 model scenarios and math checks pass. Browser/device visual testing remains outstanding.

## Resolve blocked-plan dead ends
Blocked results now list the exact triggering answers with direct edit actions. Amount correction opens the upfront/monthly question. The empty allocation chart and irrelevant stock/fund detail panels are hidden in this state. Actual answers and suitability gates remain intact.

An optional closed learning example offers funds-only (50/50 equity/debt) and higher-risk stock/fund scenarios using the entered budgets, with explicit hypothetical long-term/adult/surplus assumptions. It uses only supplied names, rounds stock quantities, observes lump-sum minima and reconciles both budgets separately. It does not mutate answers, overwrite the personal plan, execute investments or imply that essential funds are suitable for investment. Insurance guidance remains available. Tests include ₹25,000 upfront / ₹9,500 monthly, correct question links and example-state isolation.

## Active goal-first version — October 17
The entry page now loads `goal-first.js` instead of `planner.js`. This rebuild understands the goal, timeline, comfort and loss capacity before revealing percentage weights; upfront and monthly amounts are collected afterwards. Actual rupee allocations and quantities are then calculated, with editable budgets. Beginner exclusion and rigid four-stock minimum have been removed. Current model rules, assumptions and validation are documented in `GOAL_FIRST_RULES.md`; this supersedes the earlier allocation sections above. Run `node test-goal-first.cjs` for the active journey tests. Existing tests for the previous planner are historical.
