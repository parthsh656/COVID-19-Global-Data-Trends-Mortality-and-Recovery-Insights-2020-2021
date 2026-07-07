# COVID-19 Global Data Analysis(2020–2021)

## Overview
This project presents a comprehensive analysis of global COVID-19 data from January 2020 to May 2021.Using datasets on confirmed cases,deaths,and recoveries,the project transforms raw cumulative data into meaningful insights through time-series analysis,data cleaning, and feature engineering.

The goal is to understand how the pandemic evolved across countries, evaluate mortality and recovery patterns, and highlight key trends that influenced pandemic outcomes.

---

## Objectives

- Analyze the progression of COVID-19 cases, deaths, and recoveries over time  
- Identify countries with the highest mortality impact  
- Evaluate recovery efficiency using recovery-to-case ratios  
- Perform country-specific case studies (US, South Africa)  
- Detect inconsistencies and limitations in real-world pandemic data  

---

##  Dataset Description

The project uses three datasets:

- **Confirmed Cases Dataset**  
  Contains cumulative daily confirmed cases per country  

- **Deaths Dataset**  
  Contains cumulative daily death counts  

- **Recovered Dataset**  
  Contains cumulative recovery data  

  Time Range: *January 22, 2020 – May 29, 2021*  
  Coverage: *270+ regions worldwide*

---

##  Methodology

###  Data Preprocessing
- Converted wide-format datasets into long format using `melt()`
- Standardized inconsistent date formats (MM/DD/YY, DD/MM/YYYY, ISO)
- Handled missing values using forward-fill and logical imputation

---

###  Feature Engineering
- Converted cumulative data → daily values using `.diff()`
- Handled negative corrections using `.clip()` and `cummax()`
- Created monthly aggregates for trend analysis
- Derived key metrics:
  - Death Rate = Deaths / Confirmed
  - Recovery Ratio = Recovered / Confirmed

---

###  Analysis Performed

####  1. Pandemic Progression
- Monthly trends of confirmed cases, deaths, and recoveries

####  2. Mortality Analysis
- Identified top countries with highest death rates
- Used stable cumulative ratios instead of noisy averages

####  3. Recovery Analysis
- Evaluated recovery-to-case ratio over time
- Identified peak recovery months

####  4. Country Case Studies
- **United States** → Recovery ratio trends over time  
- **South Africa** → Recovery vs death comparison  

---

##  Key Insights

- Countries like **Italy and the United Kingdom** experienced high death rates due to early outbreaks and healthcare system overload.
- High death rates in some regions (e.g., Sudan) were influenced by **low testing and reporting limitations**, not necessarily higher severity.
- Recovery ratios improved over time, reflecting **better treatment protocols and healthcare adaptation**.
- Early pandemic data is unreliable due to **reporting delays and inconsistent recovery tracking**.
- Daily metrics are highly volatile; **cumulative-based metrics provide more stable insights**.

---

##  Visualizations

The project includes:
- Monthly trend analysis plots  
- Recovery vs death comparisons  
- Top countries by death rate  
- Time-series recovery ratio analysis  

*(See `/outputs/plots` for charts)*

---

##  Challenges

- Mixed date formats required custom parsing logic  
- Inconsistent recovery data reporting (especially for US)  
- Negative daily values due to data corrections  
- Many-to-many merge issues due to improper aggregation  
- Data quality limitations affecting interpretation  

---

##  Recommendations

1. **Improve Data Reporting Systems**  
   - Standardize global reporting formats  
   - Ensure consistent recovery tracking  

2. **Increase Testing Capacity**  
   - Reduces inflated death rates caused by underreporting  

3. **Early Intervention Strategies**  
   - Countries with delayed responses showed higher mortality  

4. **Strengthen Healthcare Infrastructure**  
   - Increase ICU capacity and emergency preparedness  

5. **Adopt Data-Driven Decision Making**  
   - Real-time analytics improves response effectiveness  

---

##  Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

##  Future Work

- Build predictive models for case forecasting  
- Integrate vaccination data for deeper analysis  
- Perform clustering of countries based on pandemic response  
- Develop interactive dashboards (Plotly / Power BI)  

---
