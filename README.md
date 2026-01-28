# Telecom-Customer-Analytics-Power-BI
# Overview
In the subscription-based telecom industry, Customer Churn (customers leaving) is the biggest threat to profitability. Acquiring a new customer costs 5x more than retaining an existing one.

This project is an end-to-end Business Intelligence (BI) solution designed to help management visualize where and why customers are leaving. I transformed raw customer data into an interactive Power BI Dashboard that tracks Churn Rate, Revenue at Risk, and Customer Demographics, enabling the retention team to target at-risk users proactively.

# Technologies Used
- Visualization Tool: Microsoft Power BI
- Data Transformation (ETL): Power Query (M Language)
- Calculations: DAX (Data Analysis Expressions) for creating custom measures (e.g., Churn Rate %, ARPU).
- Data Modeling: Star Schema (Fact Tables connected to Dimension Tables).

# Features & Insights
- Executive Summary: A high-level "Home" view showing KPI cards: Total Customers, Total Revenue, and Overall Churn Rate.

# Churn Analysis Page
- Breakdowns of Churn by Contract Type (Month-to-Month vs. Yearly). Insight: Month-to-month users had a significantly higher churn rate.
- Churn by Payment Method (Electronic Check users showed higher volatility).
- Customer Demographics: Analyzes the age, gender, and dependent status of customers to build "Personas" of loyal vs. churning users.

# Service Usage:
- A deep dive into which services (Streaming TV, Online Security, Tech Support) act as "sticky features" that keep customers loyal.

# Revenue Impact:
- Visualizes total charges vs. monthly charges to identify high-value customers who are at risk.

# The Process
1. Data Extraction & Cleaning (ETL):

- Loaded raw CSV data into Power BI.

- Used Power Query to clean data: Replaced Null values in "Total Charges", standardized categorical text (e.g., "No internet service" → "No"), and changed data types.

2. Data Modeling:
- Built a relational model connecting the main Customer_Fact table to reference tables (if applicable).
- Created calculated columns for specific grouping (e.g., Age Group bins).

3. DAX Implementation:
- Created Measures for dynamic reporting:
- Churn Rate = DIVIDE(Calculate(COUNT(Rows), Churn="Yes"), COUNT(Rows))
- Average Revenue Per User (ARPU)

4. Dashboard Design:
- Designed 5 specific pages: Home, Churn Analysis, Distribution & Referrals, Demographics, Revenue & Service Usage.
- Implemented "Drill-through" filters to let users click a specific city or age group and see the underlying data.

# What I Learned
- The "Why" behind the "What": It’s easy to show how many people left. It’s harder to show why. I learned to group charts (e.g., placing "Tech Support" next to "Churn") to reveal correlations visually.
- DAX Power: Mastery of CALCULATE() and FILTER() functions to create time-intelligence comparisons (though this dataset was a snapshot, the logic applies to MoM growth).
- UI/UX Design: A dashboard must be intuitive. I used navigation buttons and clear headers to ensure non-technical stakeholders could navigate without training.

# Overall Growth
- Business Acumen: This project bridged the gap between raw data and business strategy (Retention Campaigns).
- Technical: Advanced my skills in Power Query for data cleaning and DAX for complex logic, moving beyond simple "drag-and-drop" visualizations.

# How can it be improved?
- Predictive Integration: Connect this Power BI dashboard to a Python script (run inside Power BI) to display a "Predicted Churn Probability" column for each user using the Machine Learning models from my other projects.
- Real-Time Data: Connect to a live SQL database instead of a static CSV to monitor churn in real-time.
