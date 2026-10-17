# Goal-first journey — active implementation

`index.html` now loads `catalogue.js`, `app.js` (shared home, brand, insurance and export helpers), then `goal-first.js`. The previous `planner.js` is retained for history but is NOT loaded. The active rules and journey are in `goal-first.js`.

## Experience
Understand the goal → duration/optional current cost → comfort → loss capacity and surplus → client/life context → suggested percentage mix → upfront/monthly budget → actual starting plan. Choices advance automatically; input screens use Continue. Amounts are deliberately requested only after the percentage mix. Editing retains answers, while fresh start resets them. Old saved profiles are not silently mapped to new questions.

## Illustrative weights, not approved Geojit policy
- Up to 3 years, cautious preference or essential-expense loss impact: no equity, 100% debt category illustration.
- More than 3 and less than 5 years, or constrained loss capacity: 25% equity funds / 75% debt.
- At least 5 years, moderate-or-higher willingness and secure capacity: 20% stocks / 40% equity funds / 40% debt.
- At least 7 years, high willingness and secure capacity: 25% stocks / 55% equity funds / 20% debt.
- Beginner experience is not an exclusion. The experience question was removed.
- Unconfirmed surplus, essential-expense loss impact or under-18 status produces a conspicuously labelled learning illustration with an appropriate first step, not an executable/personal recommendation. Answers are never overwritten.

These percentages are application assumptions pending advisory review. General principles: https://investor.sebi.gov.in/investment-thingsbeforeinv.html . That source does not endorse these weights.

## Budget conversion
From ₹10,000: attempt four, then three, then two distinct source business groups, with equal caps inside the stock budget. Banking and NBFC share a group. Only affordable names at undated source reference prices are considered, using source order. Round to whole shares. No single-name basket. Source order is not a performance rank. Even a two-to-four-name basket is concentrated; final UI says so.

Below ₹10,000: the target stock exposure moves into the equity-fund budget, so the overall target equity exposure is retained without direct shares. Short/cautious profiles remain debt-only.

Unused stock amounts go to the debt-fund budget. Fund categories are selected by timeline/profile; highest source rating wins, then source row. Lump-sum minima and restrictions are applied. Residual money joins an existing debt fund where possible, otherwise remains explicitly unallocated.

Monthly funds use the model's TOTAL equity versus debt weights (direct-stock target included in equity fund exposure). This is independent from the upfront budget. SIP availability/minima are not in the source and are explicitly marked for verification.

## Guidance and disclosure
Actual budget pie is visible; comparison with the suggested mix, rationale, goal projection, insurance guidance/gaps and sources are closed details. Source prices are not live, costs/taxes excluded. No trades, bookings or messages are executed. Geojit CTA opens the official website only. Download includes the current plan; invitations never include private answers.

Goal calculations use effective monthly compounding, month-end contributions, adjustable return (-10 to 15%) and cost inflation (0 to 10%). Cash remainder earns zero. Goal cost is optional. Results are not forecasts or guarantees.

## Validation
Run `node test-goal-first.cjs`: 576 profile/budget scenarios plus beginner threshold, capacity restrictions, conditional labels, projection arithmetic, all screens, mix-before-money ordering, exports, back and restart, using DOM stubs. Generated result markup checked for unique IDs, form/protection outputs and closed details. Browser/physical-device visual QA remains unverified.

## Diwali route, insurance amounts and gift export
`business.js` now loads after the active goal-first module. The sixth understanding step captures personal health/life and employer health/life amounts before the suggested mix. Unknown amounts remain unknown, not zero. Family needs and health context use progressive disclosure.

After seeing the suggested mix, users choose the goal-based route or the Geojit Diwali stock-basket route. All 12 source stock picks can be explored. The latter adds an optional preferred stock budget, bounded by the model stock limit and included within—not added to—the upfront investment. Ineligible stock profiles still see the catalogue for learning. Both routes retain risk/capacity conditions.

Life need = inflated family support + debts + other future commitments − assets, floored at zero. Personal-cover gap and current gap including employer cover are shown separately. Health compares personal cover against a user/adviser-entered target; employer limits remain separate. Family members, oldest age, city, employer-covered members/shared-limit status and top-up/deductible are captured for review. No unapproved age/city-based medical cover range is invented. Health cover adequacy requires policy and needs assessment. Reference: https://irdai.gov.in/health-dept .

The downloadable HTML is self-contained: official logo embedded as PNG data URI, SVG Diwali envelope/diya illustration, SVG allocation chart, aligned stock/fund tables, insurance need/gap cards, optional goal scenario and print CSS. It uses no external images/fonts. Escaped user text prevents markup injection. Its link back to the app uses the deployment origin/path. Financial details appear only in the personal downloaded gift; invitation sharing remains generic.

Tests include capped Diwali budget reconciliation, independent employer/personal gaps, unknown data, all journey steps, embedded-logo/table/SVG export and text escaping. Generated sample markup has three allocation tables and four SVG illustrations/charts. Browser/phone visual QA remains unverified.
