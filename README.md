# ✈️ 2008 Flights Performance & Delay Analysis
**A Comprehensive Power BI Data Engineering & Analytics Project**

## 📌 Project Overview
This project transforms a massive dataset of **2.3 million flight records** into an interactive decision-making tool. 
By analyzing over **166 million minutes of delay**, the dashboard pinpoints operational inefficiencies, identifies top-performing carriers, and visualizes the "ripple effect" of late-arriving aircraft.

---

## 🛠️ Key Technical Challenges & Solutions

* **Integer-to-Time Transformation:** * **Challenge:** Time data was stored as integers (e.g., `2205` instead of `22:05`), which prevented time-intelligence analysis.
    * **Solution:** Divided values by 100 and applied data type transformations to convert them into standard Time formats for accurate calculation.
* **Engineering a Relational Schema:** * **Challenge:** The dataset lacked foreign keys to connect the Fact table with Dimensions.
    * **Solution:** Generated unique **Index Columns** in Dimension tables and performed **Merges** (Left Outer Joins) to establish a clean Star Schema.
* **Data Optimization:** * **Challenge:** Large volume of nulls and high-cardinality columns.
    * **Solution:** Replaced nulls with "Unknown" categories and removed unnecessary columns to optimize report performance and responsiveness.

---

## 🏗️ Data Architecture & Modeling
* **Schema:** Star Schema with a central Fact table and optimized Dimensions.
* **Custom Dimensions:** Built custom **Date and Time Dimension tables** to support deep-dive seasonality and time-of-day analysis.
* **Calculated Logic:** Created a custom column to categorize arrival delays (e.g., "Major Delay" > 30 mins) to highlight the most critical operational bottlenecks.

---

## 📈 Key DAX Measures
I developed custom DAX measures to provide granular performance benchmarks:
* **Total Delay:** `SUM(ArrDelay) + SUM(DepDelay)` — Captures the full impact per flight.
* **Avg Total Delay per Flight:** Identifies the average cost of delays across specific airlines or hubs.
* **Operational Benchmarks:** Created separate measures for **Average Departure Delay** and **Average Arrival Delay** to isolate where efficiency is lost.

---

## 📊 Business Insights
* **Efficiency Leaders:** **Southwest Airlines** managed the highest volume while maintaining strong relative performance.
* **Operational Gaps:** **Mesa Airlines** struggled with average delays exceeding 50 minutes.
* **Hub Performance:** Identified **Westchester County Airport** as a top performer (10 min avg delay) vs. **Yampa Valley** as a major delay origin.
* **The "Ripple Effect":** Visualized how late-arriving aircraft are the primary driver of subsequent schedule collapses.

---

## 📱 Features
* **6-Page Interactive Report:** Specialized views for Overview, Airlines, Airports, and Trends.
* **Dynamic Slicers:** Universal filtering by Airline, Airport, and Day of Month across all pages.
* **Trend Analysis:** Tracks "Change Over Time" to identify peak pressure points in the flight schedule.

---

## 📁 How to Use This Repo
1.  **View Screenshots:** Check the `/Screenshots` folder for a quick visual overview of the 6-page report.
2.  **Open the Report:** Download `Flight_Performance.pbix` to inspect the DAX measures and data model in Power BI Desktop.
3.  **View the video:** Check https://surl.li/zyinfd

---

### 💡 Contact & Connect
**Aya Hesham** [https://www.linkedin.com/in/aya-hesham-muhamad/] | [ayaheshamm2002@gmail.com]


2.  Name it `README.md`.
3.  Paste the text above.
4.  **Important:** Don't forget to upload those screenshots you showed me into the repo so the recruiter can see the "Airports" and "Airline Delay Type" pages immediately!
