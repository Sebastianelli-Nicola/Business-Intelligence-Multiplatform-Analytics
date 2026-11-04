# Multi-Platform Business Intelligence & Decision Support Systems 

[![Platforms: Qlik | Tableau | PowerBI](https://img.shields.io/badge/Platforms-Qlik_Sense_%7C_Tableau_%7C_Power_BI-blue.svg)](#-bi-platform-architectures--tools)
[![Analytics: Descriptive & Predictive](https://img.shields.io/badge/Analytics-Descriptive_%7C_Diagnostic_%7C_Predictive-green.svg)](#-project-structure--domains)
[![Dataset: 200k+ Accidents](https://img.shields.io/badge/Dataset-US_Traffic_Accidents_(209k)-orange.svg)](#-domain-1-us-traffic-accidents-analysis-qlik--tableau)
[![Dataset: 550k+ Car Sales](https://img.shields.io/badge/Dataset-US_Car_Prices_(558k)-purple.svg)](#-domain-2-us-used-car-market-power-bi)
[![Report: PDF](https://img.shields.io/badge/Report-PDF_(ITA)-red.svg)](./Relazione_BusinessIntelligence.pdf)

An enterprise-grade **Business Intelligence** portfolio implementing end-to-end data modeling, associative associative querying, interactive storytelling, and predictive forecasting across three market-leading analytics suites: **Qlik Sense**, **Tableau**, and **Microsoft Power BI**.

Developed for the *Business Intelligence & Decision Support Systems* curriculum — M.Sc. in **Computer and Automation Engineering** at **Università Politecnica delle Marche (UNIVPM)**.

>  **Full Technical Report:** Read the complete 81-page technical report (in Italian), including data dictionary mappings, DAX measures, clustering parameters, and dashboard screenshots: **[Read Complete BI Report (PDF)](./Relazione_BusinessIntelligence.pdf)**.

---

##  Project Structure & Domains

```
Business-Intelligence-Multiplatform-Analytics/
├── Qlik_Sense/     # Associative modeling, K-Means environmental clustering, accident severity
├── Tableau/        # VizQL dashboards, weekly/monthly forecasting models, roadway dynamics
├── Power_BI/       # Star schema modeling, DAX measures, US car sales & seller performance
└── docs/           # Relazione_BusinessIntelligence.pdf (Full 81-page technical report)
```

The study investigates two large-scale real-world datasets:
1. **US Traffic Accidents Dataset (>209,000 records, 24 attributes):** Investigated in **Qlik Sense** and **Tableau** to determine environmental, temporal, and human accident root causes.
2. **US Used Car Prices Dataset (>558,000 records, 16 attributes):** Modeled in **Microsoft Power BI** to evaluate vehicle pricing dynamics, body-style depreciation, regional sales volumes, and vendor efficiency.

---

##  Domain 1: US Traffic Accidents Analysis (Qlik & Tableau)

### 1. Qlik Sense — Associative Engine & K-Means Clustering
* **Data Cleansing & Ingestion:** Handled missing categories (`UNKNOWN`), generated derived time dimensions (`WeekName([crash_date])`, weekday/weekend flags), and established associative relationships without synthetic keys.
* **Core Dashboards:**
  * *Temporal Evolution:* Weekly trend lines tracing 209.3k accidents, 431.9k vehicles, 80.1k injuries, and 389 fatalities, capturing the severe mobility contraction during the COVID-19 lockdown in early 2020.
  * *Contributory Causes & Fatality:* Primary cause analysis highlighting that while driver errors (*Failing to yield, Following too closely*) dominate frequency, *Exceeding authorized speed limit* (29.3%) and *Physical driver impairment* (19.0%) dominate fatal outcomes.
  * *Multi-Vehicle Complexity:* Crash severity analysis across 1 to 9+ involved vehicles.
  * *Roadway & Illumination Conditions:* Roadway geometry cross-tabulations demonstrating that un-separated two-way roads account for the highest volume of crashes, while night conditions on unlighted roads dramatically escalate mortality rates.
  * *Machine Learning Clustering (K-Means):* 2D clustering on lighting conditions versus mean injured/fatal rates, isolating high-exposure clusters (*Daylight*, *Darkness lighted road*) from high-risk conditions (*Dusk*, *Dawn*, *Darkness*).

### 2. Tableau — VizQL Dashboards & Predictive Forecasting
* **Linear Regression & Predictive Forecasting:** Projected monthly accident trends and casualty rates across a 12-month future horizon with 95% prediction intervals.
* **Analytical Views:**
  * *Traffic Control Device Correlation:* Contrasting crash density against stop signs, railroad crossings, and traffic signals (where driver disobedience and signal timing issues drive crash volumes).
  * *Environmental Matrix:* Bubble charts and tree maps evaluating weather severity (*Clear, Rain, Snow, Ice, Fog*) and roadway surface moisture.
  * *Hour-of-Day Hourly Risk Heatmaps:* Peak collision probability localized between 13:00 and 17:00 (afternoon commute / school dismissal).
  * *First Crash Impact Classification:* Slicing angle, turning, rear-end, and fixed-object collisions against injury severity.

---

##  Domain 2: US Used Car Market (Power BI)

Interactive multi-tier analytics built using **Power BI Desktop**, star-schema data modeling, and custom **DAX** calculated measures across 558,010 commercial transactions (Mean Selling Price: $14,490):

### 1. Sales Overview & Geographic Penetration
* Choropleth geographical mapping across all 50 US States, identifying top commercial hubs (**California** at 81.05k units, Texas, Florida).
* Top-selling brands ranking (Ford, Chevrolet, Toyota, BMW, Nissan).
* Interactive cross-filtering by Year of Sale (2016–2018), Quarter (Q1–Q4), and Vehicle Odometer/Manufacturing Year (1990–2015).

### 2. Seasonality, Monthly Trends & Projections
* Monthly cyclicality identifying consistent transaction surges in Spring (April–May) and seasonal deceleration during Winter.
* Day-of-week sales volume analysis highlighting peak retail traffic on Tuesdays and Wednesdays.
* Time-series trendlines with dynamic forecasting projections into future fiscal quarters.

### 3. Vehicle Attributes & Technical Profiling
* Transmission distribution revealing an overwhelming **96.8% automatic transmission** dominance in the US automotive landscape.
* Average selling price segmented by vehicle body style (luxury coupes and convertibles leading value; compact sedans and wagons maintaining volume).
* External color distribution treemaps (monochrome market dominance: Black, White, Silver, Grey accounting for >70% of transactions).
* Odometer mileage wear analysis across utility versus premium segments.

### 4. Seller & Dealership Performance
* Vendor volume ranking (*Santander Consumer, Avis Corporation, Hertz*) versus premium transaction pricing (*West Coast Auto Group, Viva Auto Sales*).
* Strategic segmentation distinguishing high-volume wholesale leasing vendors from high-margin luxury retailers.

---

##  BI Platform Architectures & Tools

| Component | Platform | Primary Functions |
| :--- | :--- | :--- |
| **Associative Analytics** | **Qlik Sense** | In-memory engine, multi-table associative model, K-Means clustering, KPI KPI scorecards |
| **Visual Analytics** | **Tableau Desktop** | VizQL visual query engine, time-series forecasting, scatterplots, heatmaps |
| **Data Modeling & DAX** | **Microsoft Power BI** | Power Query ETL, DAX calculated measures, interactive choropleth maps, treemaps |
| **Source Datasets** | **Kaggle / OpenData** | `traffic_accidents.csv` (209k rows), `car_prices.csv` (558k rows) |

---

##  Authors & Academic Context

Master's degree project for **Project Management e Supporto alle Decisioni — Business Intelligence Module** (A.Y. 2024/2025) — M.Sc. in Computer and Automation Engineering at **Università Politecnica delle Marche (UNIVPM)**.

* **Nicola Sebastianelli** — [GitHub](https://github.com/Sebastianelli-Nicola)
* **Daniele Giuliani**
* **Ettore Ricci**
* **Pietro Salvatore**
