# 📊 Power BI: Zomato Global Restaurant Analysis

## 📌 Project Overview
* **Goal:** To combine multiple country data sheets into one interactive Power BI report to help Zomato track total restaurants, customer ratings, and dining costs worldwide.
* **Dataset:** Multiple Excel sheets split by continents (Africa, Asia, Europe, NAM, Oceania, SAM) and a Country-Code sheet.

## 🛠️ Tools Used
* Power BI Desktop & Power Query
* **Key Visuals Used:** Map charts, Donut charts, Bar charts, and Scatter plots.

---

## ⚙️ How I Built the Project (Step-by-Step)
1. **Data Ingestion & Extraction:** Programmatically imported distinct continent-level data sheets via Power Query[cite: 16].
2. **Data Cleaning and Transformation:**  Cleared unnecessary columns, extracted separate cuisine records into an independent table and combined the different continent data sheets into a single fact table.
3. **Data Modeling:** Linked the main metrics table to separate lookup tables (`Dim_Restaurant`, `Dim_Country`, `Dim_Cuisine`) using a clean **Star Schema** to keep relationships organized.
4. **DAX Measures:** Wrote custom calculated measures to automatically count total restaurants, total votes, and calculate the average rating.
5. **Conditional Formatting:** Wrote a dynamic `SWITCH(TRUE())` color measure to automatically change the visual color of a restaurant rating based on its score (e.g., Dark Green for scores above 4.5).
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

![Data Model View](./visuals/data_model_view.png)

---

## 🖼️ Dashboard Pages Preview
Below are the screenshots of the multi-page dashboard screens built in Power BI:

### 1. Home / Title Page
![Home Page Preview](./visuals/home_page_preview.png)

### 2. Geographical Analysis Page
![Geographical Dashboard Preview](./visuals/geographical_analysis_preview.png)

### 3. Restaurant Performance Tracking Page
![Restaurant Analysis Preview](./visuals/restaurant_analysis_preview.png)

### 4. Cuisine Breakdown Page
![Cuisine Analysis Preview](./visuals/cuisine_analysis_preview.png)

*Quick Note: This dashboard is fully interactive. You can use the filter buttons on the left panel to instantly update all maps, gauges, and graphs by downloading and opening the `.pbix` workbook file.*

---

## 🚀 How to Explore this Project
* 📊 **[Download Power BI Workbook](./data/Zomato_Global_Restaurant_Analysis.pbix):** Download my master `.pbix` file to check out my data model, active canvas visual interactions, and custom DAX measures.
* 📁 **[Browse Visual Project Folders](./):** Explore the repository directory containing my raw data sheets and visual report screenshots.
