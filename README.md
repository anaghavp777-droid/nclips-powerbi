# NCLIPS Sales, Quiz Performance & Student Analytics Dashboard

An interactive Power BI report for **NCLIPS**, an NCLEX nursing exam-prep app. It combines revenue, quiz performance and student activity in one three-page dashboard so you can see what is selling, what students find hard, and how both change over time.

Built as part of my Data Analytics training at **Luminar Technolab**.

> **Note:** All data is **synthetic sample data** created for learning. It does not describe real students or payments.

## Dataset

| Table | Records |
|---|---|
| Students | 1,500 |
| Payments | 2,392 |
| Quiz attempts | 17,802 |
| Time span | 731 days |

## What I Did

- Imported data from Excel into Power BI Desktop
- Cleaned and transformed it in **Power Query (M)**: data types, trimming, removing duplicates and invalid rows
- Built a **star schema** data model with a Calendar date table and one-to-many relationships
- Wrote **DAX measures**: Total Revenue, Revenue LY (`SAMEPERIODLASTYEAR`), YoY %, Accuracy %, Conversion %, Avg Revenue per Student, and Top N using `RANKX` with a What-If parameter
- Designed a **3-page interactive dashboard** (Sales, Performance, Students) with slicers, page navigation buttons, drill-down, tooltips, a custom theme and a custom background
- Validated all numbers against the source data

## Dashboard Pages

1. **Sales:** revenue, year-over-year growth, revenue by plan, conversion
2. **Performance:** quiz accuracy by topic and question type, accuracy trend
3. **Students:** student activity, revenue per student, top performers

<!-- Add screenshots after uploading them to a screenshots/ folder:
![Sales page](screenshots/sales.png)
![Performance page](screenshots/performance.png)
![Students page](screenshots/students.png)
-->

## Key Insights (sample data)

- Revenue grew **88% year over year**, from $23,016 to $43,284
- The **Annual plan** generated the most revenue (39.3%)
- **Pharmacology** was the weakest topic (65.5% accuracy)
- **SATA** questions were the hardest (65.1%) and **MCQ** the easiest (79.2%)
- Overall quiz accuracy improved from 70.8% to 73.0%

## Tools & Skills

Power BI Desktop · DAX · Power Query (M) · Data Modeling · Star Schema · Data Visualization · Dashboard Design · Excel · Business Intelligence · KPI Reporting

## Project Structure

This repo uses the **Power BI Project (.pbip)** format, so the report and model are stored as readable text files.

```
nclips-powerbi/
├── nclips.pbip              # open this file in Power BI Desktop
├── nclips.Report/           # report pages and visuals
├── nclips.SemanticModel/    # data model, measures and Power Query
├── screenshots/             # dashboard images (optional)
└── .gitignore
```

## How to Open

1. Install the latest **Power BI Desktop**.
2. Enable **File > Options and settings > Options > Preview features > Power BI Project (.pbip) save option** if it isn't already on.
3. Clone or download this repo and open `nclips.pbip`.
4. If the report asks for the Excel data source, point it to your copy of the data file and click **Refresh**.

## Author

**Anagha V P**
[LinkedIn](https://linkedin.com/in/anagha-v-p-88488622a) · [GitHub](https://github.com/anaghavp777-droid)
