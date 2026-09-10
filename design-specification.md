# Labour Productivity Page Design Specification

## Economy-wide labour productivity

### Data source

ABS Quarterly National Accounts — June quarter 2026, Table 1: Key National Accounts Aggregates.

[View ABS release](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026)

[Download productivity source workbook](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206001_Key_Aggregates.xlsx)

Series A2304192L — GDP per hour worked: Index, seasonally adjusted. Worksheet Data1, column CB. Chart period: June 2016–June 2026.

### Calculation

**Displayed index = (published index ÷ June 2016 published index) × 100**

June 2016 published index: 98.7. June 2026 published index: 99.7; displayed index: 101.0. This means productivity is about 1.0% above its starting level, not 1.0% annual growth.

Rebasing preserves growth rates and seasonal adjustment. No further inflation adjustment is required. Use the full history from the same release when refreshing; ABS may revise earlier observations.

Matches Ben’s nominated series and use for changes over time. Index values are relative comparisons, not dollar output per hour.

## Labour productivity growth by industry

### Data sources

Quarterly National Accounts, June 2026 — Table 6: Gross Value Added by Industry, Chain volume measures. Use seasonally adjusted GVA ($ millions), worksheet Data1.

[Download industry GVA](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206006_Industry_GVA.xlsx)

Labour Account Australia, June 2026 — Industry summary table. Use seasonally adjusted “Labour Account hours actually worked in all jobs” (thousand hours), worksheet Data1.

[Download industry hours](https://www.abs.gov.au/statistics/labour/labour-accounts/labour-account-australia/jun-2026/Industry%20summary%20table.xlsx)

### Series IDs — GVA / hours worked

Agriculture, forestry and fishing (A): A2716160J / A85389792L

Mining (B): A2716163R / A85389942J

Manufacturing (C): A2716166W / A85390302J

Electricity, gas, water and waste services (D): A2716175X / A85390452R

Construction (E): A2716179J / A85390602K

Wholesale trade (F): A2716180T / A85390822L

Retail trade (G): A2716181V / A85391042T

Accommodation and food services (H): A2716182W / A85391262V

Transport, postal and warehousing (I): A2716183X / A85391482W

Information media and telecommunications (J): A2716188K / A85391842R

Financial and insurance services (K): A2716189L / A85391922R

Rental, hiring and real estate services (L): A2716190W / A85392282W

Professional, scientific and technical services (M): A2716191X / A85392502L

Administrative and support services (N): A2716585R / A85392722R

Public administration and safety (O): A2716192A / A85392872W

Education and training (P): A2716193C / A85393092A

Health care and social assistance (Q): A2716194F / A85393382X

Arts and recreation services (R): A2716195J / A85393462X

Other services (S): A2716196K / A85393752W

### Calculation

For each industry, use June quarter 2026 and June quarter 2025 from the same release vintage:

**Output per hour = (GVA in $ millions ÷ hours in thousands) × 1,000**

**Year-ended growth (%) = (output per hour in June 2026 ÷ output per hour in June 2025 − 1) × 100**

The factor of 1,000 converts the units to dollars per hour; it cancels out when calculating percentage growth. No rebasing, annualising, additional seasonal adjustment or inflation adjustment is required.

### Visual

Rank all 19 industries (ANZSIC divisions A–S) by year-ended growth, highest to lowest, including public administration and safety, education and training, and health care and social assistance. Label “Year ended June 2026”; refresh quarterly. These are industry growth rates, not contributions to national growth.

All 19 GVA and hours series pairs match Ben’s methodology note. Both inputs are seasonally adjusted; output uses chain volume measures. Compare growth within each industry over time, not dollar productivity levels between industries. Recent industry hours estimates remain subject to ABS revisions.

## Economy-wide real unit labour costs

### Data source

ABS Quarterly National Accounts — June quarter 2026, Table 42: Unit Labour Costs.

[Download real unit labour cost source workbook](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206042_Unit_Labour_Costs.xlsx)

Series A2433071F — Unit labour cost – Real, seasonally adjusted. Worksheet Data1, column I. Use the total-economy series, not the non-farm series.

### Calculation

**Displayed index = (published index ÷ 104.8) × 100**

104.8 is the published June 2016 index. June 2026 is 103.6, giving a rebased index of 98.9.

**Cumulative change since June 2016 (%) = latest rebased index − 100**

The headline therefore shows real unit labour costs 1.1% below their June 2016 level. This is the cumulative ten-year change, not an average annual growth rate.

Use the published real unit labour cost index directly; no division of component series, extra inflation adjustment or seasonal adjustment is required.

### Interpretation and alignment

Shows changes in the real cost of labour per unit of output over June 2016–June 2026. Matches Ben’s exact series and intended use. The displayed index is not a dollar cost.

Ben notes that changes over more than one year are often expressed as average annualised growth. The current chart instead uses an explicitly labelled cumulative comparison; changing to annualised growth would be a presentation decision.

**Average annualised growth (%) = [(ending value ÷ starting value)^(1 ÷ number of years) − 1] × 100**

## Market-sector annual productivity growth

### Data source

ABS Quarterly National Accounts, June 2026, Table 1, worksheet Data1: market-sector GVA per hour worked index, seasonally adjusted, series A3606058X.

[Annual-growth source workbook](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206001_Key_Aggregates.xlsx)

### Calculation

**Annual growth (%) = (published index in quarter t ÷ published index four quarters earlier − 1) × 100**

Display June 2016–June 2026; inputs start in June 2015 to calculate the first observation. No rebasing or further seasonal adjustment is required.

This is the implemented chart calculation, using rounded ABS index levels. Its June 2026 result rounds to −0.2%, whereas the ABS published annual growth used in the headline card is −0.1%. Reconcile this rounding difference before final publication; do not describe the derived chart as the published percentage-growth series.

## Headline cards

### Data source

ABS National Accounts, June 2026: “Key national accounts aggregates, percentage changes” table, using the March-to-June 2026 and June-2025-to-June-2026 columns.

[Headline growth source](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026)

GDP: +0.4% over the quarter; +2.1% over the year.

Labour productivity — market sector: +0.2% over the quarter; −0.1% over the year.

Labour productivity — economy-wide (GDP per hour worked): 0.0% over the quarter; −0.2% over the year.

Use these published percentages directly; no rebasing, annualising or additional seasonal adjustment. ABS “−” means nil or rounded to zero and is displayed as 0.0%.

For quarterly updates, Table 1 percentage-change series are GDP A2304370T, market-sector productivity A3606054R, and economy-wide productivity A2304392F. Annual cards use the published through-the-year column, not the rounded-index calculation used in the annual-growth chart.

### Presentation

GDP is a separate group. One shared Labour productivity panel contains Market sector and Economy-wide subgroups, each showing quarterly and annual growth. Both groups include ABS source hyperlinks. The headline strip follows the original pale-blue styling, with simple headings and thin dividers. Financial-year comparisons are also shown for productivity: 2024–25 compared with 2023–24, market sector −0.2% and economy-wide −0.7%. Use the published percentages from the Australian System of National Accounts 2024–25 key figures table directly. These compare full financial years, rather than June quarters; no annualisation or extra seasonal adjustment is applied. Source: https://www.abs.gov.au/statistics/economy/national-accounts/australian-system-national-accounts/2024-25

## Current layout and presentation

One page, 3508 px wide × 2480 px tall, automatically fitted to the browser. The wireframe starts with the headline cards. There is no masthead, navigation tabs, preview toolbar, Print/PDF button or separate implementation-notes section.

Left column, top to bottom: market-sector annual productivity growth; economy-wide productivity index; economy-wide real unit labour costs.

Right column: all 19 industries, ranked by year-ended productivity growth, spanning all three chart rows.

Each chart presents its active title, a permanent pale-plum Title automation callout, then a subtitle containing the measure, units, seasonal adjustment, baseline and comparison period as applicable. Sources and caveats sit below the plot. Callouts explain proposed automation; automatic title generation is not yet implemented.

Market-sector callout: automate rose/fell, annual percentage change and reporting quarter. Economy-wide productivity and real unit labour cost callouts: automate percentage change and above/below the fixed June 2016 baseline. Industry callout: rank the latest results to select industry names and growth rates; adapt wording if all industries rise or fall. Handle ties, rounded zero and missing data; avoid automated causal or good/bad interpretations.

Charts use HTML and CSS, Aptos with Arial fallback, Dark Eucalyptus (#5D7A38) lines, Graphite (#404246) context bars and Plum (#62165C) for the industries named in the title. Individual chart borders are removed; gridlines are light and endpoints directly labelled. The industry column is slightly wider so its current headline fits on one line. Check physical font sizes and wide chart proportions in the final Power BI/PDF output.

## Methodology review and remaining decisions

Ben’s note confirms the economy-wide productivity index, all 19 industry input pairs and the real unit labour cost index used here. The industry calculation matches his method; the chart displays growth rates rather than cross-industry dollar levels.

Ben’s note does not explicitly specify the aggregate market-sector productivity series. Confirm A3606058X with Econ Branch if formal endorsement is required; do not treat the note as approval of every chart-design choice.

The market-sector annual-growth chart’s −0.2% and headline card’s −0.1% differ because the chart is calculated from rounded indexes. This remains unresolved and must be reconciled or clearly explained before final publication.

The real unit labour cost headline uses cumulative change, whereas Ben describes average annualised growth as a common convention for longer periods. The current wording is explicit; no annualisation has been applied.

