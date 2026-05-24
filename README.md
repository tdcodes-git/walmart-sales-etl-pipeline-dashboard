# walmart-sales-etl-pipeline-dashboard
An end-to-end data transformation (ETL) pipeline using Power Query and an interactive data analytics dashboard in Excel.

# Comprehensive Walmart Sales Transformation & Analytical Dashboard

An end-to-end Data Engineering and Business Intelligence showcase. This project demonstrates the systematic pipeline execution required to convert a heavily unstructured, corrupted retail dataset into a structured tabular database using **Excel Power Query (M-Engine)**, followed by multi-dimensional analytical modeling and an interactive executive presentation layer.

## 📌 Project Architecture
1. **Data Source:** Disorganized operational retail entries across multiple brick-and-mortar stores.
2. **ETL Pipeline:** Power Query ingestion, schema isolation, structural correction, value sanitization, and category mapping.
3. **Analytical Processing:** Multi-variable pivot aggregations (Store performance, Holiday seasonality tracking, Macroeconomic elasticity models).
4. **Presentation Layer:** Dynamic executive analytical dashboard.

---

## 🛠️ Step-by-Step Technical Breakdown

### Phase 1: Problem Identification (The Messy Raw Data)
The initial raw dataset presented severe structural and typing defects that would break standard production database ingestion engines or downstream machine learning models:
* **Structural Pollution:** Metadata headers, summary row indicators (`Store1`, `Store2`, `total`), and string-based counts (`Yes`, `no`, `Three`) injected directly into the data matrix rows.
* **Corrupted Chronological Inconsistencies:** Dual formatting flaws mixing `YYYY-MM-DD` and `DD-MM-YYYY` formats interchangeably.
* **Anomalous Values:** Numeric performance attributes corrupted with text strings (e.g., `"neg. fuel Price"`) and written-out text-based currencies (`"5000 USD"`, `"Thirty Thousand"`).
* **Sparse Matrix Gaps:** Arbitrary null row gaps breaking continuous aggregation functions.

#### Raw Data Integrity Visual Check:
File records showing raw dataset clutter and format inconsistencies:
* See file: `messy_dataset_before_screenshot.PNG`
* See file: `messy-dataset_before_screenshot_2.PNG`
* See file: `messy-dataset_before_screenshot_3.png`

---

### Phase 2: The Power Query ETL Pipeline
To clean the data repeatably, a strict ETL pipeline was developed using **Excel Power Query** to isolate the data and enforce transformations:

1. **Row & Structural Cleansing:** Stripped off row clutter, eliminated isolated textual noise, and isolated the pure fact table records.
2. **Date Format Standardisation:** Resolved dual locale formatting issues by parsing the values into a singular unified standard date datatype.
3. **Value Sanitization:** Built conditional logic steps to extract numeric float types out of text-polluted strings, resolving errors such as the `"neg. fuel Price"` entries.
4. **Dimensional Schema Enrichment:** Transformed binary `Holiday_Flag` integers (`0` / `1`) into human-readable categorical strings (`Holiday` / `Non-Holiday`) to optimize the dashboard filtering layer.

#### ETL Pipeline Operations & Structured Output:
The applied transformation steps inside Power Query and the resulting structured tabular database layout can be inspected here:
* See file: `Structured_dataset_PowerQuery_after.PNG`
* See file: `Structured_dataset_PowerQuery_CLEANED_DATA_after.PNG`

---

### Phase 3: Analytics & Strategic Data Modeling
Using the finalized database table, data models were generated via automated Pivot Tables to aggregate **$520,777,723.32** in transactions. Key performance dimensions evaluated include:

* **Store Output Divergence:** Isolated Store 2 as the absolute volume driver with over **$262M+** in sales, vastly outperforming Store 3 ($42.6M).
* **Holiday Operational Impact:** Seasonality tracking reveals non-holiday periods accounted for $481.6M vs. $39.1M across holiday operational cycles.
* **Macroeconomic Sensitivity Analysis:** Grouped revenue across exact Fuel Price tiers, revealing sales peaking at the lower price elasticity band (`$2.514 - $2.764`) at **$116.7M**.

---

### Phase 4: Interactive Executive Dashboard
The final step bridges backend engineering with visual business intelligence. The dashboard leverages clean visual hierarchies, linked multi-chart pivots, and interactive slicers to filter store performance metrics on demand.

#### Final Interactive Presentation Dashboard:
* See file: `Dashboard_screenshot.PNG`

---

## 📈 Tools & Technical Skills Featured
* **Advanced Data Engineering & ETL:** Excel Power Query, M-Language transformations, Type-casting, Data Hygiene.
* **Analytical Modeling:** Pivot Tables, Tiered Groupings, Macroeconomic Sensitivity Profiling.
* **UI/UX & Visualization:** Executive Corporate Dashboards, Interactive Slicer Syncing.
