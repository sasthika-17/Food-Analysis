# Food-Analysis
Power BI portfolio project analysing 388 online food delivery customer records: demographics, income segments, feedback and postal-area concentration. Built with Power Query and DAX.

# Online Food Delivery Customer Analysis

A Power BI data analytics portfolio project that explores who uses online food delivery, how satisfied they are, and where they are located, based on a 388-record customer survey dataset.

> **Portfolio project:** built for learning and demonstration. It is not a company or client engagement.

---

## Dashboard Preview

![Customer overview](images/01_customer_overview.png)
![Income and household](images/02_income_household_segments.png)
![Location and interpretation](images/03_location_interpretation.png)

---

## Project Overview

The report turns raw customer survey records into a 3-page interactive Power BI dashboard. It profiles customers by occupation, age, income and household, compares feedback across segments, and maps customer concentration by postal area.

## Business Objective

Help a food delivery business understand its customer base so it can:

- Identify its core customer groups
- Find segments with higher dissatisfaction
- See which postal areas are best represented

## Dataset Overview

| Item | Detail |
|---|---|
| File | `data/online_food_delivery_dataset.csv` |
| Records | 388 customer records |
| Postal areas (Pin codes) | 77 |
| Fields | Age, Gender, Marital Status, Occupation, Monthly Income, Educational Qualifications, Family size, Customer Type, Latitude, Longitude, Pin code, Output, Feedback |
| Feedback | 317 Positive, 71 Negative |

**Limitations (also stated in the dashboard):**
- Each row is one survey record, not a verified unique person.
- There are no orders, spend or dates, so order frequency is not measured.
- Income is provided as bands, not exact amounts.
- Customer Type lines up exactly with family size (1 = New, 2-3 = Regular, 4-6 = Frequent), so it reflects household size rather than measured ordering behaviour.

## Tools Used

- **Power BI Desktop**
- **Power Query**
- **DAX**

## Data Cleaning Performed

- Standardised category labels for readability, e.g. `Self Employeed` to *Self-employed*, `House wife` to *Homemaker*, `Below Rs.10000` to *Below INR 10,000*
- Removed stray whitespace in the Feedback values (e.g. `Negative `)
- Grouped customers into age bands (18-20, 21-25, 26-30, 31-35) and ordered income bands logically
- Retained repeated profiles rather than deleting them, and documented this on the dashboard

## Power Query Transformations

<!-- TODO: replace with the actual applied steps from Power Query Editor -->
Add the actual steps from your Power Query Editor (Applied Steps) here.

## DAX Measures Used

<!-- TODO: replace with the actual measures and count from the .pbix -->
Measures behind the dashboard KPIs: Total Customers, Frequent Customers, Regular Customers, Positive Feedback %, Negative Feedback Rate, Average Age, Average Family Size, Pin Codes Represented.

## Dashboard Features

- **3 pages:** Customer Overview, Segments (Income & household), Location & interpretation
- **Slicers** for Gender, Occupation, Monthly Income, Customer Type and Feedback that apply across all pages
- **KPI cards:** Total Customers (388), Frequent (146), Regular (218), Positive Feedback (81.7%)
- **Charts and tables:** stacked bars, donut, age-by-gender columns, feedback bars, income and household charts, top 10 postal areas and a sortable postal-area table
- **"How to read this report"** panel and a baseline finding callout to guard against over-interpretation

## Key Business Insights

1. **Customers are young and mostly students.** 207 of 388 records (53%) are students; the average age is 24.6 and the 21-25 band is the largest.
2. **Satisfaction is high overall.** 81.7% of feedback is positive (317 of 388).
3. **Lower-income customers are the least satisfied.** Negative feedback is 44.0% for those earning below INR 10,000 (11 of 25), versus 9.1% for customers with no income. The group is small, so it needs further investigation.
4. **Working customers are less satisfied than students.** Negative feedback is about 28% for employees and 30% for self-employed customers, versus 10% for students.
5. **Families are small.** The average family size is 3.28, and 69% of records are single.
6. **Customers are geographically concentrated.** 77 postal areas appear, but the top 10 hold about 35% of records. Area 560009 leads with 36 records.
7. **Some postal areas deserve a closer look.** 560034 (36.4% negative, 11 records) and 560075 (33.3%, 9 records) stand out, though sample sizes are small.

## Skills Demonstrated

- **Power BI** dashboard design and interactive reporting
- **Power Query** data preparation
- **DAX** measures for KPIs
- **Data Cleaning** and standardisation
- **Data Analysis** and segmentation
- **Data Visualization** for non-technical audiences
- **Business Insights** with honest limits on what the data can support


## How to Open the Power BI Project

1. Download or clone this repository.
2. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows).
3. Open `dashboard/Food_Delivery_Analysis.pbix`.
4. If prompted, point the data source to `data/online_food_delivery_dataset.csv` (Home > Transform data > Data source settings).
5. Use the slicers on the left to explore all three pages.
