# ✈️ Project 5: Airlines Performance & Delay Analysis in Aviation Industry via Power BI Dashboard Analytics

**Domain:**  
Aviation and Transportation. 

![Image](https://github.com/user-attachments/assets/028326d8-451e-49b8-9bca-63239119ff17)

Author: Susan Ho  
Date: 2026-01-15  
Tools Used: Power BI  

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#1-background--overview)  
2. [📂 Dataset Description & Data Structure](#2-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#3-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#4-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#5-final-conclusion--recommendations)
6. [💡 Deep dive into Route & Airline Optimization](#6-deep-dive-into-route--airline-optimization)
7. [✨ More information](#7-more-information)

---
## 1.📌 Background & Overview
The goal of this project is to build an **analytic and tactical dashboard** to help airline leadership and aviation authorities understand their operational efficiency, specifically focusing on flight delays and cancellation patterns. By linking flight schedules with actual departure/arrival data and specific delay reasons, this report aims to optimize route planning, improve on-time performance (OTP), and propose actionable tactics for operational improvement.

Through this project, we:
- Process flight, airport, and airline data to build a comprehensive data model.
- Construct prototypes, continuously iterating to address stakeholder reporting needs.
- Link operational metrics (Departure Delay, Arrival Delay, Taxi-In/Out) with key performance indicators (On-Time Delivery, Cancellation Rate).
- Provide analytical conclusions and tactical recommendations to optimize airline performance.
  
### 👤 Project Audience
This project is built for:
- **Airline Operations Directors & Aviation Authorities** who need a clear, data-driven view of national and regional airspace efficiency and major delay drivers.
- **Flight Schedulers / Analysts** to track granular metrics like Average Delay by Airline, Route, or Time of Day, identifying areas for immediate tactical shift in scheduling.

### 🏢 Business Context and ❓Question 
This industry operates within the aviation sector, primarily across major and regional US airports. Airlines operate thousands of daily cross-country flights and face significant logistical challenges related to weather, air systems, security, and internal carrier operations.
To ensure resources and fleet utilization are managed efficiently, management requires consolidated insights to answer the following business questions:

1. **How efficiently are airlines operating across the national network?**
- Purpose: Understanding the overall on-time performance at a glance.
- Why it matters: Stakeholders need to know if delays are systemic or isolated to specific airlines or airports.
- Data perspective: Track Scheduled vs. Actual Times, Delay Minutes, Cancellation Counts, and Carrier Performance.

2. **What are the primary drivers of flight delays and cancellations?**
- Purpose: Linking top-level delays to their root causes (e.g., Weather, Security, National Air System).
- Why it matters: It shows whether delays are within the airline's control (e.g., late aircraft, carrier delay) or external, allowing for better strategic buffer planning.
- Data perspective: Assess Cancellation Reasons, Airline Delay, Weather Delay, Air System Delay, and Security Delay.

3. **Which routes and airlines should we optimize or investigate further?**
- Purpose: Optimizing the flight schedules to minimize operational waste and improve customer satisfaction.
- Why it matters: Identifying "Star" punctual routes/airlines guides future operational benchmarks, whereas discovering underperforming hubs dictates resource reallocation.
- Data perspective: Delay severity (minutes), Taxi-in/out times per Airport, and flight volume cross-analysis.

---

## 2.📂 Dataset Description & Data Structure
### 🔍 Data source Overview
The dataset captures the domestic flight operations, airline catalogs, airport locations, and granular delay/cancellation performance across the US for the year 2015. 

Across the primary tables, the dataset encompasses millions of flight records and essential lookup dimensions:
- **`fact-flights`**: Over 5.8+ million records
- **`dim-airports`**: ~322 records
- **`dim-airlines`**: ~14 records
- **`dim-cancellation_codes`**: 4 records

### 🔗 Data Relationships & Model Design
The Power BI data model follows a **fact–dimension structure** to support efficient analysis and reporting.

#### Data Model Structure
The data model is structured as a **Star Schema** within Power BI, integrating multiple data sources to enable cross-filtering between flight operations and geographic/carrier outcomes.
- **Fact Tables (Transactional Data)**:
  - **`fact-flights`**: Records the core flight transactions. Contains granular flight details including `YEAR`, `MONTH`, `DAY`, `AIRLINE`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`, `SCHEDULED_DEPARTURE`, `DEPARTURE_TIME`, and actual delay metrics (`DEPARTURE_DELAY`, `ARRIVAL_DELAY`). This table serves as the primary source for calculating Total Volumes, Average Delays, and On-Time Performance.

- **Dimension Tables (Lookup Data)**:
  - **`dim-airports` (Airport Master):** The central location dimension linking flights to geography. Contains attributes like `IATA_CODE`, `AIRPORT` (Name), `CITY`, `STATE`, `LATITUDE`, and `LONGITUDE`.
  - **`dim-airlines` (Carrier Overview):** Contains top-level airline information, linking the airline `IATA_CODE` to the full `AIRLINE` name (e.g., United Air Lines Inc., Delta Air Lines).
  - **`dim-cancellation_codes` (Reason Master):** Maps cancellation indicators to human-readable descriptions (`A` = Airline/Carrier, `B` = Weather, `C` = National Air System, `D` = Security).
  - **`dim_date` (Date Dimension):** A standard time-intelligence table extracted from the YEAR, MONTH, DAY fields, linking to the fact table, enabling chronological analysis and Month-over-Month comparisons.

#### Table Relationships

---
## 3.🧠 Design Thinking Process


---
## 4.📊 Key Insights & Visualizations

---
## 7.✨ More information 
#### 🛠️ Workflow
This project unfolds through an iterative process heavily reliant on big data processing and aviation intelligence modeling:
* **Round 1: Data Processing & Modeling:** Cleaning raw flight logs (over 5.8M rows), mapping airline codes and airport locations, handling the complex delay allocations, and building a DAX-heavy robust data model.
* **Round 2: Iterations:** Gathering feedback to iterate on the operational dashboards significantly across multiple iterations (Punctuality view, Root Cause view, Hub Efficiency view).
* **Round Final:** Polishing the final dashboard, performing dynamic analysis on the insights discovered, drawing tactical recommendations for Flight Ops, and presenting via an analytical walkthrough.

