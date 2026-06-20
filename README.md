# Power BI Analytics Portfolio

This repository contains **one Power BI file (`.pbix`) that houses two separate, end-to-end analytical dashboards**, built side by side as two distinct sets of report pages within the same file. Each project has its own data tables, its own DAX measures, and its own multi-page narrative — they are kept logically separate even though they live in a single `.pbix`.

> **Why one file instead of two?** Power BI Desktop allows multiple report pages inside a single `.pbix`, each with its own visuals and (optionally) its own subset of tables in the data model. Rather than splitting into two files, this project uses **page grouping and naming conventions** to keep the two dashboards distinct and easy to navigate within one file — useful for reviewers who want to see both projects without opening multiple files.

---

## How the file is organized

The report pages are named with an `A_` or `B_` prefix so they group together and sort correctly in the page-navigation pane:

| Page (in .pbix) | Project | What it shows |
|---|---|---|
| `A_Executive Summary` | A — Sales | Headline KPIs, sales trend, sales by product line, sales by country |
| `A_Product & Deal Analysis` | A — Sales | Treemap by product, deal size mix, order status, top 10 products |
| `A_Customer & Geography` | A — Sales | Sales by territory, country map, top customers |
| `A_Marketing & Targets` | A — Sales | Advertising vs. sales scatter, salesperson gauges, monthly KPI trend |
| `B_Carbon Emissions` | B — Sustainability | Global CO2 KPI, CO2 by region, CO2 treemap, top emitters |
| `B_Eco Footprint` | B — Sustainability | Eco-footprint vs biocapacity map and scatter, countries in ecological debt |
| `B_Plastic & Population` | B — Sustainability | Plastic waste funnel, EU population waterfall |

Each group also uses its own colour theme so the two projects are visually distinguishable at a glance: **blue** for Project A, **green/teal** for Project B.

---

## Project A: Vehicle Sales Performance Dashboard

**Business question:** How is our vehicle & parts business performing — by time, product, geography — and are we hitting our sales targets?

- **Data:** 2,832-row transactional sales dataset (2003–2005, 19 countries, 7 product lines), plus supporting files for marketing spend, salesperson targets, and monthly KPI tracking.
- **Tools/skills shown:** Power Query cleaning (mixed date formats, null removal), a calculated `Sales` column (`QUANTITYORDERED × PRICEEACH`), DAX measures (Total Sales, YoY Growth, Avg Order Value), a `CALENDARAUTO()` date table for time intelligence, and interactive slicers (Year, Territory, Product Line, Deal Size).
- **Key insights:** Classic Cars is the top-performing product line; the USA is the largest single market; most orders ship successfully, but Cancelled/On Hold orders flag an operational gap worth investigating.

## Project B: Global Sustainability & Carbon Footprint Dashboard

**Business question:** How do countries compare on carbon emissions, ecological footprint, and plastic pollution — and what's the gap between resource use and resource availability?

- **Data:** Four standalone reference datasets — CO2 emissions by country (193 countries), biocapacity vs. ecological footprint per person (177 countries), a 5-stage global plastic waste funnel, and EU population change by member state (29 states).
- **Tools/skills shown:** Advanced Power BI chart types (filled map, treemap, funnel, waterfall) used deliberately to match each dataset's story, plus DAX measures for ecological-debt counting and percentage breakdowns.
- **Key insights:** China, the USA, and India together account for roughly half of global CO2 emissions; only ~2.8% of plastic produced each year reaches the ocean (still 8 million tonnes); several EU member states are losing population.

---

## Tools Used

- **Power BI Desktop** — report building, data modelling, DAX
- **Power Query** — data cleaning and transformation
- **Excel** — source data and project documentation

## How to Run

1. Download Power BI Desktop (free) from [powerbi.microsoft.com](https://powerbi.microsoft.com).
2. Open `Sales_Sustainability_Portfolio.pbix` — both projects load together since they're in one file.
3. Use the page navigator on the left to jump between the `A_` (Sales) pages and `B_` (Sustainability) pages.
4. Use the slicers at the top of each page to filter that page's visuals interactively.

## Skills Demonstrated

- Data cleaning & transformation (Power Query)
- Data modelling (relationships, calculated columns, date table)
- DAX (measures, time intelligence, `DIVIDE`, `CALCULATE`, `FILTER`)
- Data visualisation — 10+ chart types, each chosen for a specific analytical purpose
- Managing two independent analytical narratives within a single Power BI file
- Documentation & version control (GitHub)

## Author

[Harshit Panchal] | [www.linkedin.com/in/harshit-panchal-955887205] | [harshitpanchal2277@gmail.com]
Open to Data Analyst / Business Intelligence Analyst roles.
