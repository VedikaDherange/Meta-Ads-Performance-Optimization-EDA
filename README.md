# 📊 Pinnacle Meta Ads Campaign Dataset – Marketing Analytics & Performance Optimization

**An end-to-end Marketing Analytics and Exploratory Data Analysis (EDA) project focused on Meta Ads campaign performance, audience targeting, advertising efficiency, and data-driven optimization using Microsoft Excel and Python.**

---

## 📌 Project Overview

This project focuses on cleaning, transforming, and analyzing a Meta Ads campaign dataset to evaluate advertising performance and generate actionable marketing insights.

The dataset includes:

- 10,000+ rows of advertising data
- Approximately 50 structured columns after preprocessing
- Embedded JSON-based audience targeting specifications
- Campaign-level, Ad Set-level, and Ad-level performance metrics

The raw dataset required extensive preprocessing because of semi-structured JSON fields, redundant system-generated metrics, hourly and weekday breakdowns, missing values, and inconsistent data types.

The primary objective was to transform raw advertising data into an analysis-ready dataset using Excel and perform advanced Exploratory Data Analysis (EDA) in Python to identify high-performing campaigns, optimize advertising spend, and support better marketing decisions.

## 🎯 Project Objectives

- Clean and transform complex Meta Ads campaign data.
- Extract meaningful information from embedded JSON targeting specifications.
- Analyze campaign, Ad Set, and Ad-level performance.
- Evaluate key advertising KPIs such as CTR, CPC, conversion rate, and ROI.
- Identify high-performing and underperforming advertisements.
- Compare advertising performance across platforms and time periods.
- Develop actionable recommendations for campaign optimization.

## 🛠️ Tools & Technologies

| Category | Tools & Technologies |
|---|---|
| Data Cleaning | Microsoft Excel |
| Data Analysis | Python |
| Data Manipulation | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Reporting | Excel Pivot Tables |
| Version Control | Git, GitHub |
| Development Environment | Jupyter Notebook |

---

## 🧹 Phase 1: Excel Data Cleaning & Structuring

Microsoft Excel was used for initial data preprocessing, standardization, feature engineering, and preparation of the dataset for analysis.

### 1. JSON Column Handling

- Extracted audience targeting information, including age ranges, interests, behaviors, and geographical locations.
- Flattened important information from nested JSON structures.
- Removed raw JSON columns after extracting relevant fields.
- Simplified the dataset for easier analysis.

### 2. Data Standardization

- Converted dates, currency, and numeric columns into appropriate formats.
- Ensured Ad ID uniqueness.
- Cleaned text-based `NaN` values to prevent parsing issues during Python analysis.
- Standardized data for consistent calculations.

### 3. Column Reduction & Optimization

- Removed columns containing approximately 80–90% missing values.
- Dropped hourly breakdown columns that could be recalculated during analysis.
- Removed weekday-specific columns that could be derived from dates.
- Eliminated redundant or derivable metrics, including Ad Rank and Top 25% CPC.
- Retained important columns required for performance analysis.

### 4. Feature Engineering

Created additional calculated metrics:

- Engagement Rate (24-hour, 7-day, and overall)
- Conversion Rate (24-hour, 7-day, and overall)
- Monthly performance column
- Date-range and time-based derived columns

---

## 📊 Phase 2: Excel Pivot Analysis

Excel Pivot Tables were used to summarize advertising performance across different dimensions.

### Platform-Level Analysis
- Total Spend
- Total Conversions
- Average CPC
- Conversion Rate

### Campaign-Level Performance
- Payments
- Cost per Landing Page View (CPLPV)
- ROI %
- CTR %

### Daily Performance Analysis
- Day-wise payments
- CPC trends
- Conversion trends

---

## 🐍 Phase 3: Python-Based Exploratory Data Analysis

Python was used to validate calculated KPIs, investigate data quality, identify performance patterns, and generate visual insights.

### Libraries Used
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Analysis Performed

- KPI recalculation and validation
- Missing-value and anomaly checks
- Statistical distribution analysis
- Platform performance comparison
- Campaign efficiency benchmarking
- Correlation analysis
- Outlier detection
- Identification of high-performing and underperforming ads

---

## 📈 Key Findings & Marketing Insights

### 1. Ad-Level Performance Analysis

Out of 237 Ads:

| Performance Decision | Number of Ads | Evaluation |
|---|---:|---|
| Continue | 24 | High CTR, low CPC, and strong conversion rate |
| Pause | 183 | Below target performance benchmarks |
| Discontinue | 30 | Low CTR, high CPC, and poor conversion performance |
| **Total** | **237** | |

### Platform Performance

Recommended ads to continue:

| Platform | Ads Recommended |
|---|---:|
| Facebook | 6 |
| Instagram | 7 |
| Threads | 11 |

**Key Insight:** Threads emerged as the strongest-performing platform based on the selected ad-level performance benchmarks.

**Recommendation:** Prioritize budget allocation toward better-performing ads while continuously monitoring platform-level results.

---

### 2. Best Day to Run Ads

**Tuesday emerged as the highest-performing day.**

Key observations:

- 308 Payments
- Lowest CPC: ₹3.50
- Above-average conversion rate

**Recommendation:** Consider increasing budget allocation on Tuesdays while monitoring performance over subsequent periods.

---

### 3. Campaign-Level Analysis

#### 🏆 Best Performing Campaign: VM || Delhi NCR || Traffic

- Lowest CPC: ₹1.16
- Highest Payments: 568
- Conversion Rate: 0.77

**Recommendation:** Continue and consider scaling this campaign due to its strong payment performance and cost efficiency.

#### ⚠️ Campaign Requiring Optimization: Web App | Conversion

- Highest Spend: ₹181K+
- CPC: ₹13.26
- Conversion Rate: 0.37

**Recommendation:** Review audience targeting, advertising creatives, and campaign costs to improve conversion efficiency.

#### 📣 Brand Awareness Campaign: VM Brand Awareness

- 8.79% of total spend
- Reported cost-efficiency metric: ₹0.08
- Poor direct conversion performance

**Recommendation:** Evaluate this campaign primarily on awareness and reach objectives rather than direct payment conversions. The reported ₹0.08 metric should be interpreted using its original KPI definition.

#### ❌ Least Performing Campaigns

- ToF Engagement
- Straight Outta

Both campaigns generated zero payments despite consuming advertising budget.

**Recommendation:** Discontinue or restructure these campaigns to reduce unnecessary spending.

---

### 4. Ad Set-Level Analysis

#### 🏆 Top Performing Ad Set: Women - Clubbed Audience

- Payments: 567
- Lowest CPLPV: ₹2.30
- Conversion Rate: 0.81

**Recommendation:** Consider scaling this audience segment while monitoring its cost and conversion performance.

#### RMK - Waitlist

- Conversion Rate: 1.05
- CPLPV: ₹18.50
- Slightly higher CPC with strong conversion performance

**Recommendation:** Maintain and optimize the budget based on its conversion efficiency.

#### ❌ Underperforming Ad Sets

The following ad sets generated zero payments despite consuming advertising budget:

- Dating Apps
- Entrepreneurship Insta
- Travel Insta
- Interest-Based Dinner

**Recommendation:** Stop or restructure these ad sets to prevent further budget leakage.

---

### 5. Top Performing Ads

#### Top 5 Ads Based on Spend Contribution and Payments

1. Monkey UGC
2. Ad – 1 (5 Strangers)
3. Saturday Night
4. Ranveer
5. Instagram Post – Latest StepOut Dinner

#### 🥇 Top 3 Most Efficient Ads

1. Monkey UGC
2. Saturday Night
3. Ranveer

Key performance characteristics:

- High payment generation
- CPLPV below ₹1.50
- Conversion Rate approximately 0.70

**Recommendation:** Prioritize these creatives for further testing and potential budget scaling.

---

## 📐 KPI & Metric Formulas

The following KPIs were used to evaluate advertising performance.

### Core Performance Metrics

| KPI | Formula |
|---|---|
| Click-Through Rate (CTR) | (Clicks / Impressions) × 100 |
| Cost Per Click (CPC) | Total Spend / Total Clicks |
| Conversion Rate (CR) | Conversions / Clicks |
| Cost Per Acquisition (CPA) | Total Spend / Total Conversions |
| Cost Per Landing Page View (CPLPV) | Total Spend / Landing Page Views |
| Engagement Rate | Total Engagements / Impressions |
| Return on Investment (ROI) | ((Revenue − Spend) / Spend) × 100 |

*Note: Conversion Rate can also be calculated using impressions as the denominator when measuring impression-to-conversion rate. The denominator should always be stated clearly.*

### Time-Based Metrics

**Daily Performance**
- Daily Impressions = Sum of impressions grouped by date.
- Daily Conversions = Sum of conversions grouped by date.
- Daily CPC = Daily Spend / Daily Clicks.

**Monthly Performance**
- Monthly Spend = Sum of spend grouped by month.
- Monthly Conversion Rate = Monthly Conversions / Monthly Clicks.

### Benchmark Comparison Metrics

**Performance vs Group Average**

Metric Ratio = Ad Metric / Group Average Metric

- Ratio below 0.85: Underperforming
- Ratio above 1.15: Overperforming
- Ratio between 0.85 and 1.15: Near the group average

**Performance vs Top 25th Percentile**

Metric Ratio = Ad Metric / Top 25th Percentile Benchmark

Used to compare individual ad performance against stronger-performing ads.

### Decision Threshold Logic

| Decision | Criteria |
|---|---|
| Continue | Above-average CTR, below-average CPC, and strong conversion rate |
| Pause | Near-average CTR, moderate CPC, and inconsistent conversions |
| Discontinue | Conversion Rate below 0.01, high CPA, or zero payments despite spend |

These thresholds represent the project's analytical decision rules.

---

## 📗 Excel Formula Implementations

```excel
CTR = (Clicks / Impressions) * 100

CPC = Spend / Clicks

Conversion Rate = Conversions / Clicks

CPA = Spend / Conversions

ROI = ((Revenue - Spend) / Spend) * 100
```

*Calculations involving zero denominators should be handled appropriately to avoid division errors.*

---

## 💼 Business Value & Recommendations

This project demonstrates how marketing data can be transformed into meaningful business decisions.

Key business recommendations:

- Allocate more budget toward consistently high-performing ads.
- Optimize campaigns with high CPC and low conversion rates.
- Monitor audience segments to identify profitable targeting opportunities.
- Evaluate awareness campaigns using awareness-focused KPIs.
- Reduce unnecessary spending on campaigns generating no payments.
- Continuously monitor campaign performance using standardized KPIs.

## 🚀 Skills Demonstrated

- Data Cleaning and Preprocessing
- JSON Data Extraction and Transformation
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Statistical Analysis
- KPI Calculation and Validation
- Excel Pivot Table Analysis
- Data Visualization
- Marketing Performance Analytics
- Campaign Optimization
- Data-Driven Decision Making

## 🔮 Future Enhancements

- Develop machine learning models to predict campaign performance.
- Build automated campaign performance reporting.
- Apply audience segmentation techniques.
- Integrate real-time advertising data.
- Develop interactive marketing performance dashboards.

---

## 👩‍💻 Author

**Vedika Dherange**

**Technical Skills:** Python | SQL | Excel | Pandas | NumPy | Matplotlib | Seaborn | Data Analytics | Exploratory Data Analysis

**Project Focus:** Marketing Analytics | Meta Ads Performance Optimization | Data-Driven Decision Making

---

⭐ If you find this project useful, consider giving the repository a star!

*This project demonstrates an end-to-end marketing analytics workflow, from raw data cleaning and transformation to exploratory analysis, performance benchmarking, and actionable campaign optimization recommendations.*
