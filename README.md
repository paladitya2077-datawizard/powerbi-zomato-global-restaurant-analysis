# 📊 Power BI: Zomato Global Restaurant Analysis

## 📌 Project Overview
* **Goal:** To combine multiple country data sheets into one interactive Power BI report to help Zomato track total restaurants, customer ratings, and dining costs worldwide.
* **Dataset:** Multiple Excel files containing a central Fact Table, Country Codes, and regional data split by 6 continents (Asia, Africa, Europe, Oceania, NAM & SAM).

## 🛠️ Tools Used
* Power BI Desktop & Power Query
* **Key Visuals Used:** Map charts, Donut charts, Bar charts, and Scatter plots.

---

## ⚙️ How I Built the Project (Step-by-Step)
1. **Data Ingestion & Extraction:** Programmatically imported distinct continent-level data sheets via Power Query[cite: 16].
2. **Data Cleaning and Transformation:**  Cleared unnecessary columns, extracted separate cuisine records into an independent table and combined the different continent data sheets into a single fact table.
3. **Data Modeling:** Linked the main metrics table to separate lookup tables (`Dim_Restaurant`, `Dim_Country`, `Dim_Cuisine`) using a clean **Star Schema** to keep relationships organized.
4. **DAX Measures:** Wrote custom calculated measures to automatically count total restaurants, total votes, and calculate the average rating.
5. **Conditional Formatting:** Wrote a dynamic `SWITCH(TRUE())` color measure to automatically change the visual color of a restaurant rating based on its ratings (e.g., Dark Green for ratings above 4.5).
6. **Dashboard Navigation:** Designed 4 separate report pages (Home, Geographical Analysis, Restaurant Analysis, and Cuisine Analysis) and added a functional sidebar navigation menu to easily click between them.

---

## 💡 Key Insights (What I Found)
* **Insight 1 (Global Numbers):** The dataset tracks 9,551 restaurants across 6 continents, 15 countries, and 140 cities. Asia is the biggest market, with New Delhi alone holding over 5,400 active restaurants.
* **Insight 2 (Ratings Split):** Most restaurants fall under the "Average" rating slab (39.13%), followed by "Not Rated" locations at 22.49%.
* **Insight 3 (Cost vs. Rating):** Looking closely at sub-regions like Indonesia, mid-range priced restaurants actually receive much higher vote counts from customers compared to ultra-expensive ones.
* **Insight 4 (Cuisine Trends):** North Indian is the most popular cuisine served globally in this dataset, followed closely by Chinese and Fast Food.

---

## 📐 Data Model Structure
Below is a screenshot of the relational star schema showing how the fact and dimension tables link together:

![Data Model View](visuals/Screenshot%202026-07-14%20080644.png)

---

## 🖼️ Dashboard Pages Preview
Below are the screenshots of the multi-page dashboard screens built in Power BI:

### 1. Home Page
![Home Page Preview](visuals/Screenshot%202026-07-14%20080514.png)

### 2. Geographical Analysis Page
![Geographical Dashboard Preview](visuals/Screenshot%202026-07-14%20080523.png)

### 3. Restaurant Performance Tracking Page
![Restaurant Analysis Preview](visuals/Screenshot%202026-07-14%20080534.png)

### 4. Cuisine Breakdown Page
![Cuisine Analysis Preview](visuals/Screenshot%202026-07-14%20080556.png)

*Quick Note: This dashboard is fully interactive. You can use the filter buttons on the left panel to instantly update all maps, gauges, and graphs by downloading and opening the `.pbix` workbook file.*

---

## 🚀 How to Explore this Project
* 📊 **[Download Power BI Workbook](dashboard/Aditya_Pal_Zomato_Restaurant_Analysis_Project.pbix):** Download my master `.pbix` file to check out my data model, active canvas visual interactions, and custom DAX measures.
* 📁 **[Browse Visual Project Folders](/data):** Explore the repository directory containing my raw data sheets.
