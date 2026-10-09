## Repository Structure- 
README.md
 Projects--
 1. Spotify\
    [View the PDF Document](Joanna_1250258235_DescriptiveAnalyticsReport.pdf)\
    [View the ipynb file](Spotify%20songs%20Analysis%20(2).ipynb)\
    [View the cleaned dataset](spotify_cleaned_dataset.pdf)

 2. IBM Cognos Analytics\
    [Link to practicals folder ibm cognos](https://us3.ca.analytics.ibm.com/bi/?perspective=content&folder=.public_folders%2Fpracticals&nav_filter=true)\
    [View Report 1](Report%201.pdf)\
    [View Report 2](Report%202.pdf)\
    [View Report 3](Report%203%20(filtered-second).pdf)\
    [View Report 4](Report%204.pdf)\
    [View Report 5](RetailPulse%20Sales%20Prompt%20Report%205.pdf)\
    [View Dashboard](Dashboard%206.pdf)

 4. Power BI\
    
    [View evidences](RetailPulse_Analysis.pdf)

        
# Spotify-Descriptive-Analytics-Report-

# 🎧 Audio Aura: Wrapped

**Decoding Listener Behaviour and Chart-Topping Trends**

A descriptive analytics study of what 80 Spotify tracks reveal about genre, mood, release trends and popularity. Built with Python, Pandas, Matplotlib and Seaborn.

---

## 📌 Overview

This project applies descriptive analytics to a real-world music dataset to understand how **genre, audio features, artist identity and release timing** relate to a track's popularity on Spotify. It ends with practical suggestions for playlist curators, artists and labels, and a roadmap towards predictive analysis.

| | |
|---|---|
| **Course** | BCA, Data Science & Artificial Intelligence (2nd Year), BCADS23 |
| **Subject** | Descriptive Analytics |
| **Faculty** | Ms Monika Rao |
| **University** | Babu Banarasi Das University |

---

## 📊 Dataset

- **Source:** [30,000 Spotify Songs (Kaggle)], it's reproducible).
- **Cleaning:** kept 12 relevant columns, converted duration from milliseconds to minutes, engineered `release_year`, and fixed 3 tracks whose release date was a bare year. No duplicates and very few missing values; one genuine loudness outlier (−36.5 dB) was kept.

---

## 🎯 Objectives

1. Which genres dominate the sample?
2. Which artists and tracks are most popular, and why?
3. How have duration and popularity changed across release years?
4. How do popularity and audio features (danceability, energy, valence, acousticness) relate?
5. What makes each genre musically distinct?
6. Which audio features move together?

---

## 🔍 Key Findings

- **Genre concentration:** rap (26%), pop (19%) and r&b (16%) make up 61% of the sample; rock is smallest at 10%.
- **Popularity is artist-driven:** Camila Cabello (87) and The Chainsmokers (85) lead; most others sit between 73 and 79.
- **Audio features barely predict popularity:** the strongest correlation with popularity is danceability at r = 0.15.
- **Genres have audio fingerprints:** EDM has the lowest acousticness (0.04) and highest energy (0.80); rap has the highest danceability (0.72).
- **Songs got shorter:** average duration fell from 6.3 min (1978) to a stable 3.3–5.1 min band from the 2000s onward.
- **Production features move together:** energy vs loudness is +0.60 and energy vs acousticness is −0.50.

---

## 📈 Visualisations

| # | Chart | Purpose |
|---|---|---|
| 1 | Top 8 artists (bar) | Average popularity by artist |
| 2 | Genre distribution (donut) | Share of each genre |
| 3 | Audio traits by genre (grouped bar) | What makes each genre unique |
| 4 | Lowest 10 tracks (line) | Do low-popularity tracks share audio traits? |
| 5 | Top artists by playtime (bar) | Total listening minutes per artist |
| 6 | Mood vs energy and tempo vs loudness (scatter) | Quadrant view of sound and production |
| 7 | Popularity and duration by year (dual line) | Trends over time |
| 8 | Correlation matrix (heatmap) | Relationships between features |

---

## 🧮 Statistical Methods

- **Aggregation:** genre totals and average popularity
- **Central tendency:** mean 44.1, median 48.0, mode 0 (7 tracks) for popularity
- **Spread:** range, standard deviation (popularity SD = 24.1)
- **Frequency distribution:** release-year decades (the 2010s account for 72.5% of the sample)

---

## ⚠️ Limitations

- Small sample (n = 80), so small genres like rock are "a snapshot of this sample", not the full picture.
- Year-level averages for 1991 and 2013 rest on a single track each; the dips to zero are sampling artefacts.
- The source playlists lean towards upbeat, radio-friendly music, which limits generalisation to all of Spotify.

---

## 🔮 Next Steps (Predictive)

Popularity prediction, genre auto-tagging, song-length forecasting and similarity-based recommendation engines.

---

## 📚 References

- Arvidsson, J. (2020). *30,000 Spotify songs* [Data set]. Kaggle.
- McKinney, W. (2010). Data structures for statistical computing in Python.
- Hunter, J. D. (2007). Matplotlib: A 2D graphics environment.
- Waskom, M. L. (2021). Seaborn: Statistical data visualization.

---

# 🛒 RetailPulse: IBM Cognos Analytics Practicals

A hands-on series of reports and a dashboard built in **IBM Cognos Analytics** on a 400K-row synthetic retail sales dataset. It moves from simple list reports to grouped lists, a crosstab, a prompt-driven report and finally an interactive customer-insights dashboard.

---

## 📌 Overview

| Item | Detail |
|---|---|
| **Tool** | IBM Cognos Analytics (Reporting + Dashboards) |
| **Data source** | `synthetic_sales_data_400k.csv` (uploaded as a data module / package) |
| **Period covered** | 1 Jan 2023 to 31 Dec 2024 |
| **Currency** | ₹ (INR) |

### Dataset fields

`Product_ID` · `Sale_Date` · `Sales_Rep` · `Region` · `Sales_Amount` · `Quantity_Sold` · `Product_Category` · `Unit_Cost` · `Unit_Price` · `Customer_Type` · `Discount` · `Payment_Method` · `Sales_Channel` · `Region_and_Sales_Rep`

**Dimensions in the data:** 4 regions (East, North, South, West) · 5 sales reps (Alice, Bob, Charlie, David, Eve) · 4 categories (Clothing, Electronics, Food, Furniture) · 2 channels (Online, Retail) · 2 customer types (New, Returning).

---

## 🗂️ What's Inside

| # | Output | Type | What it shows |
|---|---|---|---|
| 1 | **RetailPulse First Report** | List report | Regions and product categories with `Sales_Amount`, plus region subtotals and an overall total |
| 2 | **RetailPulse Second Report** | Grouped list | Region → Sales Rep → Product Category with `Quantity_Sold` and `Sales_Amount`, with subtotals at every level |
| 3 | **Report 3 (filtered)** | Filtered list | A filtered version of the grouped list *(add your filter condition here)* |
| 4 | **RetailPulse Fourth Report** | Crosstab | Regions (rows) × Product Categories (columns), measuring `Sales_Amount` and `Quantity_Sold` with totals |
| 5 | **RetailPulse Sales Prompt Report** | Prompt report | Crosstab driven by a prompt page: Region, date range and a cascading Sales Rep prompt |
| 6 | **Customer Insights Dashboard** | Dashboard | Region filter, total card, sales-channel bar chart and a New vs Returning trend line |

---

## 🔍 Key Results

- **Overall sales:** ₹28,514,051,718.71 across 400K transactions.
- **Region totals:** East ₹7.131B · North ₹7.132B · South ₹7.133B · West ₹7.117B, almost perfectly even.
- **Category totals (crosstab):**

| Category | Sales Amount | Quantity Sold |
|---|---|---|
| Clothing | ₹7,138,801,521.35 | 2,548,720 |
| Electronics | ₹7,109,945,168.08 | 2,539,276 |
| Furniture | ₹7,133,332,433.30 | 2,557,359 |
| Food | ₹7,131,972,595.98 | 2,547,152 |

- **Prompt report (East, filtered run):** total ₹738,568,467.40, with Food (₹188.0M) and Furniture (₹184.8M) alongside Clothing (₹186.0M) and Electronics (₹179.7M).
- **Dashboard:** 400K total transactions, Online and Retail channels roughly equal at about 200K each, and New vs Returning customers hovering around 250–300 per day.

> 💡 The numbers are very uniform because the dataset is **synthetic**. The goal is mastering the tool, not business conclusions.

---

## 🧩 Skills Demonstrated

- Building **list reports** and grouping with subtotals and grand totals
- **Multi-level grouping** (Region → Rep → Category)
- **Filters** at report and widget level
- **Crosstabs** with multiple measures and totals
- **Prompt pages**: value prompt, date-range prompt, cascading prompt, linked to report filters
- **Dashboards**: KPI card, bar chart, line chart, and a shared **Region filter widget** cross-filtering every widget
- Exporting to **PDF** and fixing layout/pagination

---

## 📊 Dashboard Widgets (Practical 6)

| Widget | Purpose |
|---|---|
| Region filter | Cross-filters all widgets on the canvas |
| Total Customers | Count of transactions (`Product_ID`) |
| Customers by Sales Channel | Bar chart, Online vs Retail |
| New vs Returning Customers | Line chart of `Customer_Type` over `Sale_Date` |

**Assumptions:** the dataset has no customer ID or loyalty field, so *customers* are measured as transaction counts and *segment* is represented by `Sales_Channel`.

---

## ⚠️ Notes & Limitations

- Synthetic data, so results are near-uniform and not real-world insight.
- No customer or loyalty columns; the dashboard uses transactions and sales channel as proxies.
- Date grouping depends on the Cognos version; the trend line is daily unless grouped by month.

---

# 📊 RetailPulse Analysis: Power BI Sales Dashboard

An interactive, four-page **Power BI** report on a 400,000-row synthetic retail sales dataset. It covers data cleaning in Power Query, a star-schema data model, time-intelligence measures (YTD, last year, YoY growth) and **row-level security** so each regional manager sees only their own region.
---

## 📌 Overview

| Item | Detail |
|---|---|
| **File** | `RetailPulse_Analysis.pbix` |
| **Source data** | `synthetic_sales_data_400k.csv` |
| **Period** | Jan 2023 to Dec 2024 (730 days) |
| **Currency** | ₹ (INR) |

---

## 🧱 Data Preparation (Power Query)

Applied steps on `synthetic_sales_data_400k`:

1. Source, then **Promoted Headers**
2. **Changed Type** (twice: numbers, dates and text)
3. **Removed Blank Rows**
4. **Removed Duplicates**
5. **Replaced Value** (data fixes)
6. **Renamed Columns** (friendly names, e.g. `Sales Date`, `Sales Amount`)
7. **Added Conditional Column**: `Sale Size` (for example, Large)

---

## 🗺️ Data Model (Star Schema)

```
Product (4 rows) ──1──┐
Store   (20 rows) ─1──┼──*── Sales (400,000 rows)
Date    (730 rows) ─1─┘
```

| Table | Role | Key fields |
|---|---|---|
| **Sales** | Fact | Product ID, Sales Date, Sales Rep, Region, Sales Amount, Quantity, Product Category, Unit Cost, Unit Price, Customer Type, Discount, Payment Method, Sales Channel, Region and Sales Rep, Sale Size, Sales per Unit |
| **Date** | Dimension | `CALENDAR(MIN(Sales[Sales Date]), MAX(Sales[Sales Date]))` with Year, Month Number, Month Name |
| **Product** | Dimension | Product Category (Clothing, Electronics, Food, Furniture) |
| **Store** | Dimension | Region, Region and Sales Rep (4 regions × 5 reps = 20 rows) |

All relationships are one-to-many from each dimension into `Sales`.

### Key measures

`Total Sales` · `Total Quantity` · `Sales YTD` · `Sales LY` · `YoY Growth %` · `Average Order Value` · `Region Share %`

---

## 📄 Report Pages

| Page | What it shows |
|---|---|
| **1. Dashboard** | Region slicer, **Total Sales** card, **Total Sales by Month** line chart and **Total Sales by Product Category** bar chart |
| **2. Trends** | Month × Year matrix of Total Sales, Sales YTD, Sales LY and YoY Growth %, plus a combined line chart of the same measures |
| **3. Select Region & Year** | Region slicer and Year range slider driving a detail table (Count of Product ID, Payment Method, Product Category, Region and Sales Rep, Sum of Sales Amount) |
| **4. Store Detail** | Animated scatter plot: **Average Order Value vs Sum of Unit Price** per Region and Sales Rep, with a play axis stepping through regions |

---

## 🔐 Row-Level Security

Roles are defined under **Modeling → Manage roles** and tested with **View as**, for example:

- **North Manager** sees only North data
- **South Manager** sees only South data

The Region slicer shows only the allowed region, and every visual (including the Total Sales card) recalculates for it. Check the roles list in the file for the full set.

---

## 🔍 Key Insights

- **Sales are evenly spread:** each region contributes about ₹7.1bn of the ₹28.5bn total (South ≈ ₹7.133bn, North ≈ ₹7.132bn).
- **Categories are balanced:** Furniture, Electronics, Clothing and Food each bring in about ₹1.8bn per region.
- **No strong seasonality:** daily and monthly sales fluctuate within roughly ₹6M–₹14M with no clear trend, as expected for synthetic data.
- **South detail view:** 100,023 transactions in the South region, totalling ₹7.13bn.

> 💡 The data is synthetic, so values are near-uniform. The project is about modelling and Power BI technique, not business conclusions.

---

## 🛠️ Skills Demonstrated

- Power Query cleaning and transformation
- Star-schema modelling and relationships
- **DAX:** calculated tables, calculated columns, measures, time intelligence (YTD, LY, YoY)
- Slicers, matrix, line, bar, scatter (play axis) and card visuals
- **Row-level security** with role testing
- Multi-page report design and navigation

---

## ⚠️ Notes & Limitations

- Synthetic data, so no real-world conclusions.
- There is no customer ID or loyalty field in the data.
- Some Indian-format numbers (₹ lakh/crore grouping) appear in tables because of regional settings, while cards use ₹ bn.

---

## 🔗 Related

The same dataset was also analysed in **IBM Cognos Analytics** (list reports, crosstab, prompt report and dashboard) for comparison.

---

## 👩‍💻 Author


**Joanna**, BCA (Data Science & AI), Babu Banarasi Das University
