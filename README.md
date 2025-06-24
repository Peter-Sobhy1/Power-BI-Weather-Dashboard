# 🌦️ Interactive Weather Dashboard (Power BI)

This project is a fully dynamic Power BI dashboard that visualizes weather data (temperature and chance of rain) across three major Egyptian cities: **Cairo**, **Giza**, and **Alexandria**. The data is fetched from a live weather API and automatically refreshed every three hours.

**Link** for the dashboard: https://app.powerbi.com/view?r=eyJrIjoiYTQ1OWZhOGEtNDRiYi00YWQ5LThiY2MtZTI3ZDA0YzVkYmFiIiwidCI6IjJiYjZlNWJjLWMxMDktNDdmYi05NDMzLWMxYzZmNGZhMzNmZiIsImMiOjl9

![Dashboard Image](https://github.com/Peter-Sobhy1/Weather-Power-BI-Dashboard/blob/main/Assets/Weather%20Dashboard%20Image.png?raw=true)

## 🔧 Project Overview

- **Cities Monitored**: Cairo, Giza, Alexandria  
- **Data Source**: Connected to a live **Weather API** using an API Key  
- **Refresh Schedule**: Configured to refresh **every 3 hours** using the Power BI service (as shown in the image below)
- **Dashboard Features**:
  - Dynamic **temperature trends** per weekday
  - Dynamic **chance of rain** visualization
  - **Forecast** for the next 7 days
  - **Air quality** Index
  - Conditional formatting using **icons and color-coded dots**
  - **Fully dynamic visuals** that update based on API values

## 📊 Data Model Design

![Data Model!](https://github.com/Peter-Sobhy1/Weather-Power-BI-Dashboard/blob/main/Assets/Data%20Model.png?raw=true)

The data model is optimized for performance and accuracy using star schema design principles. It includes:

- **Fact Table**:
  - `Current`
- **Dimension Table**:
  - `Locations`
  - `Forecast_Hour`
  - `Forecast_Day`
 
  
### 📐Query Structure
![Qeuries!](https://github.com/Peter-Sobhy1/Weather-Power-BI-Dashboard/blob/main/Assets/Queries.png?raw=true)

- Three separate queries for each city (`Cairo`, `Giza`, `Alexandria`)
- These were **appended** using "Append as New" to create a unified `MasterTable`
- The `MasterTable` is used to generate:
  - Reference queries (dimension & fact)
  - Cleaned dimensions by removing duplicates and unnecessary columns
- **Load disabled to data model** for:
  - The three city queries
  - `MasterTable` (used only as a base for referenced queries)


## ⚙️ Automation

- The report uses **scheduled refresh** on the Power BI Service every 3 hours (8 times a day)
- Time zone is set to **(UTC+02:00) Cairo**
![Scheduled Refresh](https://github.com/Peter-Sobhy1/Weather-Power-BI-Dashboard/blob/main/Assets/Schedule%20Refresh.png?raw=true)

## 📁 Files

- `.pbix` Power BI report file
- API key configuration is done securely within Power BI and **not exposed** in this repository
- Data model, query structure, and refresh logic screenshots are included

## 📈 Visual Highlights

- Weekday-wise temperature chart
- City-based weather comparison
- Real-time updates with API integration
- Enhanced user experience with intuitive icons and tooltips

---

## 📌 Note

Make sure to replace the API key with your own if you plan to republish or fork the project. The key should be securely managed.

---







Let's stay in touch!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/peter-sobhy/)
