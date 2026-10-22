# Diwali Sales Data Analysis 📊

## Project Overview
This project explores Diwali sales data using Python to understand customer purchasing patterns, sales performance, and product demand. The analysis focuses on customer demographics, gender, age groups, states, marital status, occupation, product categories, and product-level orders.

The goal is to turn raw sales data into actionable insights that can help a business understand its customers and plan future festive-season campaigns.

## Objectives
- Clean and prepare the dataset for analysis.
- Explore customer demographics and purchasing behaviour.
- Compare spending across gender and age groups.
- Identify states contributing the most orders and sales.
- Explore spending patterns by marital status and occupation.
- Identify popular product categories and products by order volume.
- Present findings using charts and summary statistics.

## Dataset
- **Original dataset size:** 11,251 rows × 15 columns
- **Rows after removing missing values:** 11,239
- **Columns after removing unused blank columns:** 13
- **Missing values handled:** 12 missing values in `Amount` were removed.
- **Data source:** Diwali Sales Data CSV used in the notebook.

The dataset includes fields such as `User_ID`, `Cust_name`, `Product_ID`, `Gender`, `Age Group`, `Age`, `Marital_Status`, `State`, `Zone`, `Occupation`, `Product_Category`, `Orders`, and `Amount`.

## Tools & Technologies
- **Python** — analysis
- **Pandas** — data cleaning, grouping, aggregation and summaries
- **NumPy** — numerical operations
- **Matplotlib** — charts and plotting
- **Seaborn** — statistical visualizations
- **Jupyter Notebook** — analysis workflow

## Data Cleaning & Preparation
The notebook includes the following preparation steps:
1. Loaded the CSV file using Pandas.
2. Removed the unused `Status` and `unnamed1` columns.
3. Checked missing values across columns.
4. Removed rows with missing values using `dropna()`; 12 rows were removed because `Amount` was missing.
5. Converted `Amount` to an integer data type.
6. Renamed `Marital_Status` to `Shadi` for subsequent analysis.
7. Used descriptive statistics to review numeric and categorical columns.

> Note: The notebook uses `Shadi` as the renamed marital-status column. In the analysis, `0` and `1` are compared as the two marital-status groups; their exact labels should be confirmed from the original dataset's data dictionary before interpreting them as married or unmarried.

## Analysis & Key Findings

### 1. Gender
- Female customers accounted for **74,335,853** in total recorded purchase amount.
- Male customers accounted for **31,913,276**.
- Female customers contributed substantially more purchase amount than male customers in this dataset.

### 2. Age Group
Total purchase amount by age group:

| Age Group | Total Amount |
|---|---:|
| 26–35 | 42,613,442 |
| 36–45 | 22,144,994 |
| 18–25 | 17,240,732 |
| 46–50 | 9,207,844 |
| 51–55 | 8,261,477 |
| 55+ | 4,080,987 |
| 0–17 | 2,699,653 |

- The **26–35** age group generated the highest recorded purchase amount.
- The **36–45** and **18–25** groups were the next largest contributors.

### 3. State-wise Orders and Purchase Amount
The highest order counts in the notebook were:

| State | Total Orders |
|---|---:|
| Uttar Pradesh | 4,807 |
| Maharashtra | 3,810 |
| Karnataka | 3,240 |
| Delhi | 2,740 |
| Madhya Pradesh | 2,252 |
| Andhra Pradesh | 2,051 |
| Himachal Pradesh | 1,568 |
| Kerala | 1,137 |
| Haryana | 1,109 |
| Gujarat | 1,066 |

- **Uttar Pradesh** recorded the highest order count and the highest total purchase amount among states in the analysis.
- Maharashtra and Karnataka followed in both order count and total purchase amount.

### 4. Marital-status Group and Gender
The grouped purchase amounts were:

| Marital-status code (`Shadi`) | Gender | Total Amount |
|---:|:---:|---:|
| 0 | F | 43,786,646 |
| 1 | F | 30,549,207 |
| 0 | M | 18,338,738 |
| 1 | M | 13,574,538 |

- Female customers had a higher recorded purchase amount than male customers in both marital-status groups.
- Group `0` had a higher total purchase amount than group `1` for both genders.
- Confirm the meaning of the `0` and `1` codes against the dataset documentation before assigning marital-status labels.

### 5. Occupation
The notebook compares customer counts and total purchase amount across 15 occupation categories. Its recorded interpretation identifies **IT Sector, Healthcare, and Aviation** among the prominent customer occupation groups.

### 6. Product Categories
The notebook explores customer counts and purchase amount across 18 product categories. Its recorded interpretation highlights **Food, Clothing & Apparel, and Electronics** as prominent categories in the sales analysis.

### 7. Product-level Orders
The notebook groups order counts by `Product_ID` and displays the top 10 products by total orders in a bar chart. This helps identify products with the highest order volume.

## Visualizations
The notebook includes charts for:
- Customer count by gender
- Total purchase amount by gender
- Customer distribution by age group and gender
- Purchase amount by age group
- State-wise order counts
- State-wise purchase amount
- Marital-status group and gender comparison
- Customer count and purchase amount by occupation
- Product-category distribution and purchase amount
- Top 10 products by order count

## Business Recommendations
Based on the observed patterns, a business could:
1. **Tailor campaigns by audience:** Test targeted festive campaigns for customer groups that contributed higher purchase amounts, especially female customers and the 26–35 age group.
2. **Prioritize strong-performing states:** Review inventory and campaign allocation for Uttar Pradesh, Maharashtra, and Karnataka, which led the state-wise order analysis.
3. **Plan category-level promotions:** Evaluate suitable offers and stock levels for Food, Clothing & Apparel, and Electronics.
4. **Personalize messaging carefully:** Explore occupation and demographic segments to test which campaigns work best, rather than assuming every customer in a group behaves the same way.
5. **Track product demand:** Use the top-product order analysis to support replenishment and product-level promotions.
6. **Measure campaign results:** Compare future campaign conversion, order count, and purchase amount to determine whether these actions improve performance.

These are recommendations based on the patterns explored in this dataset, not proof of causation or a forecast of future sales.

## How to Run
1. Clone or download this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Place the CSV dataset in the appropriate location or update the file path in the notebook.
4. Open and run `Diwali Sales data Analysis.ipynb` in Jupyter Notebook.

## Project Structure
```text
Diwali-Sales-Data-Analysis/
├── Diwali Sales data Analysis.ipynb
├── Diwali Sales Data.csv        # Add this file if you are permitted to share it
└── README.md
```

## Conclusion
The analysis found that female customers and customers aged **26–35** contributed the largest recorded purchase amounts. **Uttar Pradesh, Maharashtra, and Karnataka** led the state-wise order analysis. The notebook also highlights IT Sector, Healthcare, and Aviation among prominent occupation groups, and Food, Clothing & Apparel, and Electronics among prominent product categories.

These findings can help guide customer segmentation, festive campaign planning, inventory reviews, and further sales analysis.

## Skills Demonstrated
`Python` · `Pandas` · `NumPy` · `Data Cleaning` · `Exploratory Data Analysis (EDA)` · `Data Visualization` · `Seaborn` · `Matplotlib` · `Business Insights`

---
*Created as a data analytics portfolio project using Python and Jupyter Notebook.*

