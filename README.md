# Superstore-Sales-Analysis-PowerBI
This is my Week 2 project for the AnalystLab Africa Internship. I built an interactive 2-page dashboard to analyze retail sales, focusing on profitability and regional trends.

Week 3 Update: Strategic Growth & Profitability Analysis
In the third week of this project, I moved beyond basic reporting to Diagnostic Analysis.
New Features Added:
Advanced DAX Measures: Created formulas for Year-over-Year Sales Growth, Average Discount rates, and Customer Acquisition counts.
Strategic Dashboard (Page 3): Developed a new "Advanced Insights" page featuring:
Scatter Plot Analysis: Visualizing the "Danger Zone" where high discounts (over 20%) lead to negative profit.
Loss-Maker Investigation: Identifying the "Bottom 5" products (specifically the Cubify 3D Printer) that are draining company profits.
Customer VIP Tracking: Identifying the Top 5 customers by revenue contribution.
Time-Based Comparison: Implemented a dual-line chart to compare Sales and Profit trends month-over-month.
Key Recommendation: The organization should implement a "Discount Ceiling" of 20% and audit the pricing of high-volume, low-margin items like 3D Printers.

Week 4 Update: HealthConnect Experience Lab
This week marks the start of the HealthConnect Experience Lab. I am pivoting from retail analysis to healthcare, focusing on improving patient appointment attendance.
Tasks Completed:
Initial Analysis: Reviewed the HealthConnect dataset to understand patient "No-Show" patterns.
DQA Planning: Developed a plan to handle missing distance and wait-time data using neighborhood averages.
KPI Definition: Proposed new metrics like the No-Show Rate (%) and SMS Effectiveness Ratio.
Strategic Planning: Investigated the psychological impact of "Wait Fatigue" and end-of-day scheduling.
Next Steps: In Week 5, I will begin data transformation and building the HealthConnect interactive dashboard.

🚀 Week 5: Practical Implementation Complete
EDA Result: Confirmed a massive "Wait Fatigue" trend where no-shows spike to 57.4% for long lead-times.
Channel Insight: Identified SMS as the most effective reminder channel (52.0% show rate).
Architecture: Successfully deployed a monochrome teal-themed analytical foundation.


## 🏥 Week 6: HealthConnect Advanced Analytics & Data Science Integration
### 📌 Overview
Week 6 focused on cross-track collaboration with the Data Science team (Pod 01) to integrate predictive Machine Learning feature drivers into an executive two-page Power BI dashboard suite to reduce patient no-shows.
### 📊 Dashboard Preview
| Page 1: Executive Overview | Page 2: Advanced Analytics |
| :---: | :---: |
| ![Executive Overview](Week%206/Dashboard_Page1_Executive_Overview.png) | ![Advanced Analytics](Week%206/Dashboard_Page2_Advanced_Analytics.png) |
### 🔑 Key Findings & Data Science Integration
* **Dataset Scope**: Analyzed **4,737 active, non-cancelled appointments** (51.2% baseline no-show rate) following the exclusion of 263 cancelled records.
* **Lead Time Fatigue (`wait group`)**: Appointments scheduled **>14 days in advance (Extended)** face a critical **57.4% no-show rate**, compared to **26.6%** for short lead times (0–3 days).
* **Patient Type Risk (`is_new_patient`)**: Returning patients exhibit a higher no-show rate (**51.4%**) than first-time patients (**45.6%**).
* **Behavioral Risk Progression (`previous_no_shows`)**: Prior missed appointments strongly predict future non-attendance, scaling from **46.3%** (0 prior misses) up to **100.0%** (5 prior misses).
* **Model Validation**: Cross-track collaboration validated **Logistic Regression (61.6% accuracy)** over Random Forest (60.0%) due to its high interpretability for clinical leadership.
### 💡 Strategic Recommendations
1. **7-Day Re-Confirmation Protocol**: Implement automated multi-channel re-confirmations for bookings in the Extended wait group (>14 days).
2. **Tailored Continuity Messaging**: Tailor reminder messaging for returning patients to emphasize ongoing care plans.
3. **Channel Allocation**: Prioritize direct SMS and WhatsApp over email for long-lead appointments, where SMS reduces no-shows to **54.3%** vs. email's **59.0%**.
📁 All Week 6 report files, Power BI workbooks, and datasets are available in the [`/Week 6`](./Week%206) folder.


## 🧪 Week 7 — Analytics Testing, DAX Optimization & Cross-Track Validation

### Technical Performance & Integrity Enhancements
* **DAX Latency Reduction:** Refactored core DAX measures on Page 2 using pre-calculated variables (`VAR`), reducing visual query evaluation times from **780ms to 185ms** (a **76.3% performance increase** verified via Performance Analyzer).
* **Zero-State Handling:** Applied `ISBLANK` safety wrappers and `DIVIDE(..., 0)` logic across all KPI cards to ensure graceful `0.0%` state rendering during extreme cross-filtering.
* **UI/UX Matrix Heatmap:** Standardized the *Lead Time x Reminder Channel* matrix from raw counts to row-wise percentage heatmaps with high-contrast conditional formatting.

### Cross-Track ML Model Alignment (HC-POD 01)
* Audited and re-calibrated the rule-based Power BI **DAX Risk Engine** against the Data Science track’s **Logistic Regression Machine Learning Model** ($P > 0.50$).
* Achieved a **98.4% risk classification alignment rate** across all 4,737 active patient records (4,661 matching records).
