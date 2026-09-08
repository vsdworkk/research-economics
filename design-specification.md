# Labour Productivity Page Design Specification

## Productivity comparison

### Data sources

ABS Quarterly National Accounts — June quarter 2026

Table 1: Key National Accounts Aggregates

[View ABS release](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026)  |  [Download source workbook](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206001_Key_Aggregates.xlsx)

Both series: quarterly, seasonally adjusted. Chart period: June 2016–June 2026.

#### Market sector

Series: A3606058X

Gross value added per hour worked market sector: Index

Worksheet Data1 · Column CC

#### Total economy

Series: A2304192L

GDP per hour worked: Index

Worksheet Data1 · Column CB

### Calculation

Set June 2016 = 100 for both series (96.3 and 98.7 are the respective published index values for June 2016) :

**Market sector = (published index ÷ 96.3) × 100**

**Total economy = (published index ÷ 98.7) × 100**

**Headline change = latest rebased index − 100**

- June 2026: market sector +4.3%; total economy +1.0%.

- No further seasonal or inflation adjustment is required. Round only the displayed results; source indexes are already rounded.

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

Arts and recreation services (R): A2716195J / A85393462X

Other services (S): A2716196K / A85393752W

### Calculation

For each industry, use June quarter 2026 and June quarter 2025 from the same release vintage:

**Output per hour = (GVA in $ millions ÷ hours in thousands) × 1,000**

**Year-ended growth (%) = (output per hour in June 2026 ÷ output per hour in June 2025 − 1) × 100**

The factor of 1,000 converts the units to dollars per hour; it cancels out when calculating percentage growth. No rebasing, annualising, additional seasonal adjustment or inflation adjustment is required.

### Visual

Rank all 16 market-sector industries (ANZSIC A–N, R and S) by year-ended growth, highest to lowest. Exclude public administration, education and health (O–Q). Label “Year ended June 2026”; refresh quarterly. These are industry growth rates, not contributions to national growth.

Recent industry hours estimates are subject to ABS revisions. This calculation uses verified source series; Ben’s review of the methodology remains pending.

## GDP growth and forecast revisions

### Status

The current wireframe uses illustrative history and Scenario A/B values. The sources below are those cited by the prototype, with the required method for replacing the illustrative values.

### Data sources

ABS National Accounts, March 2026 — Table 1: Key National Accounts Aggregates. GDP, chain volume measures, seasonally adjusted ($ millions); series A2304402X. June 2026 data are now available for a refresh.

[ABS historical GDP source](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/mar-2026)

MYEFO 2025–26 — Table 1.1: Major Economic Parameters, Real GDP row (previous forecast).

[MYEFO forecast source](https://budget.gov.au/content/myefo/download/myefo-2025-26.pdf)

Budget 2026–27 — Budget Paper No. 1, Table 1.1: Major Economic Parameters, Real GDP row (updated forecast).

[Budget forecast source](https://budget.gov.au/content/bp1/download/bp1_2026-27.pdf)

### Required calculation

**Historical growth (%) = (sum of the latest four quarters of real GDP ÷ sum of the preceding four quarters − 1) × 100**

At each June quarter, this compares one financial year with the previous financial year. Use GDP levels, not a sum or average of quarterly percentage growth rates.

Forecasts are already financial-year percentage growth rates: use them directly. Do not annualise or seasonally adjust them again. Plot at financial-year endpoints; the tables do not supply a quarterly forecast path.

**Forecast revision (percentage points) = Budget forecast − MYEFO forecast for the same financial year**

For 2026–27: 1.75% − 2.25% = −0.50 percentage points. Replace Scenario A/B with the publication names when real data are implemented.

### Headline

The existing headline refers to 2026–27. The forecast tables establish the downgrade; attributing it to the Middle East conflict requires support from the accompanying economic outlook commentary.

## Market-sector annual growth — Page 3

### Data source

ABS Quarterly National Accounts, June 2026, Table 1, worksheet Data1: market-sector GVA per hour worked index, seasonally adjusted, series A3606058X.

[Annual-growth source workbook](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026/5206001_Key_Aggregates.xlsx)

### Calculation

**Annual growth (%) = (published index in quarter t ÷ published index four quarters earlier − 1) × 100**

Display June 2016–June 2026; inputs start in June 2015 to calculate the first observation. No rebasing or further seasonal adjustment is required.

This is the implemented chart calculation, using rounded ABS index levels. Its June 2026 result rounds to −0.2%, whereas the ABS published annual growth used in the headline card is −0.1%. Reconcile this rounding difference before final publication; do not describe the derived chart as the published percentage-growth series.

## Headline cards — all pages

### Data source

ABS National Accounts, June 2026: “Key national accounts aggregates, percentage changes” table, using the March-to-June 2026 and June-2025-to-June-2026 columns.

[Headline growth source](https://www.abs.gov.au/statistics/economy/national-accounts/australian-national-accounts-national-income-expenditure-and-product/jun-2026)

GDP: +0.4% over the quarter; +2.1% over the year.

Labour productivity — market sector: +0.2% over the quarter; −0.1% over the year.

Labour productivity — economy-wide (GDP per hour worked): 0.0% over the quarter; −0.2% over the year.

Use these published percentages directly; no rebasing, annualising or additional seasonal adjustment. ABS “−” means nil or rounded to zero and is displayed as 0.0%.

For quarterly updates, Table 1 percentage-change series are GDP A2304370T, market-sector productivity A3606054R, and economy-wide productivity A2304392F. Annual cards use the published through-the-year column, not the rounded-index calculation used in Page 3.

### Presentation

GDP is a separate group. One shared Labour productivity panel contains Market sector and Economy-wide subgroups, each showing quarterly and annual growth. The financial-year comparison has been removed.

## Layout options and visual coverage

Page 1 — combined market-sector and economy-wide indexes at top left; GDP forecasts below; all 16 market-sector industries on the right spanning both rows.

Page 2 — market-sector index, economy-wide index and GDP forecasts stacked on the left; the same industry chart on the right spanning all three rows.

Page 3 — market-sector annual growth, economy-wide index and GDP forecasts stacked on the left; the same industry chart on the right spanning all three rows.

Separate index charts use the same series, June 2016 = 100 rebasing, dates and shared 98–108 scale documented under Productivity comparison. Splitting the visual introduces no additional calculations.

All pages share the same headline cards and industry data. Forecast values remain illustrative until the documented ABS and Treasury inputs are implemented.


