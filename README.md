# 🎮 Video Games Sales Analysis Dashboard 
#### Amazon Web Services + Power BI project
(**Data source:** AWS S3
**Connectors:** ODBC & Amazon Athena)
## ❓ Problem Statement
The global video game industry spans multiple platforms, genres, and markets, generating billions in sales annually. However, understanding which factors drive game popularity and regional market trends remains a challenge for developers, publishers, and analysts.

## 🚀 Project Overview
This project presents an interactive dashboard built with Power BI, connecting directly to an AWS Athena data source to analyze global video game sales. The dashboard utilizes a comprehensive dataset containing attributes such as game title, genre, platform, release year, publisher, and regional/global sales figures.

The main objective is to transform raw video game sales data into visual, actionable insights for decision makers and enthusiasts. By leveraging cloud-native querying and Power BI’s dynamic visualizations, users can quickly identify top games, analyze sales trends across different regions and platforms, compare performance by genre and publisher, and track market evolution over time.

This repository serves as a complete blueprint for sales analytics in the gaming domain—addressing business questions, enhancing data-driven strategy, and demonstrating best practices for cloud-integrated analytics dashboard development.

## 📂 Dataset Details
**AWS Glue Table:** `powerbiprojectaws`

Each row represents a unique video game release.​

- Columns cover Rank (sales and popularity), Name (game title), Platform (console/system), Year (release year), Genre (category/type), and Publisher (company).​

- Sales fields include regional breakdowns: NA_Sales (North America), EU_Sales (Europe), JP_Sales (Japan), Other_Sales (other regions), and Global_Sales (total worldwide units).​

- The dataset is sourced as a CSV file from AWS Athena for cloud-based querying and analysis.​

- Contains thousands of games spanning releases from the early 1980s to present, providing wide market coverage.​

## 🔧 Data Transformation

### Key Steps
*powerbiprojectaws (AWS dataset)*
1. **Attribute names:** Promoted headers.
2. **Filtered rows:** Filtered `Rank` to remove null values.
3. **Renamed columns:** Renamed columns to match with the csv dataset in later steps.

*CSV (extra dataset)*

4. **Promoted headers:** Filtered `Rank` to remove null values.
5. **Changed datatypes:** Changed data types for `Rank` and `Sales figures`.
6. **Append queries:** Appended queries `powerbiprojectaws` and `CSV` as new table `Clubbed data`.
7. **Fixed Errors:** Fixed Errors in `Year column`.
8. **Replace values:** Replaced Null values with 0.
9. **Multipled Columns:** Used number column section to multiply existing region wise sales column with 100000.
10. **Data Profiling:** Ensured data quality by handling null values and duplicates.
11. **Relationship Setup:** Established one-to-many relationships for smooth interaction between tables.

## 📊 Report Pages & Visualizations

### 1. Overview

![Image](https://github.com/user-attachments/assets/5aee5084-779c-4754-b01a-ac43ce675f5b)

- **Purpose:** Introduces the project and provides a overview of sales in modern gaming environment look with dynamic bittons for bookarks and navigation.

- **Visuals:**
    - **Radar/Spider visual:** Comparing the sales figures across different genres, displaying the overall comparative patterns or trends in the dataset.
    ![Image](https://github.com/user-attachments/assets/ee8312e0-618a-4f1f-af4d-dd69edb82c80)
    - **Bookmark Buttons:** Buttons change the radar visual based sales in different regions of the world.
    ![Image](https://github.com/user-attachments/assets/5f1da397-e23a-4017-90b7-1e75de3abf6a)
    - **Navigation Button:** Navigate quickly to tabular visuals page of Sales to get quantified numeric figures in tabular format.
    ![Image](https://github.com/user-attachments/assets/42278d3f-0cbf-443e-89ba-ce54d8b26966)


### 3. Detailed Table 

![Image](https://github.com/user-attachments/assets/af17b738-27c9-4e47-bf7f-7032a80c5a30)

- **Purpose:** Shows detailed matrix of the sales figures to extract exact values if needed in calculations or presentations.

**Visuals:**
    - **Matrix visual:** Table-like visualization to displays data across multiple dimensions regions and genres, similar to a pivot table. Allowing to group, summarize, and drill down into sales figures, making it easier to analyze patterns, compare values, and present complex information in a clear, structured format.

### 3. Line Charts (Time series)

![Image](https://github.com/user-attachments/assets/54abaf0a-ab0a-40b9-a5a4-c7b44239fbe0)

- **Purpose:** This page is invaluable for analyzing trends, seasonal patterns, and long-term trends in data. 

- **Line chart:** Visualizing sales figure changes over time for different genre.

---

## 🌟 Key Insights

- **Cloud-Integrated Analytics:** Direct connection from Power BI to AWS Athena using ODBC enables seamless querying of large-scale video game sales data stored in AWS S3, ensuring near real-time insights.

- **Comprehensive Dataset:** Covers 40+ years of video game releases with detailed attributes including game title, platform, genre, publisher, release year, and regional sales breakdowns (North America, Europe, Japan, other regions).

- **Dynamic Visualizations:** Interactive visuals including radar charts, line charts, and detailed matrices allow users to explore sales trends across various dimensions such as region, genre, platform, and publisher.

- **Data Transformation & Quality:** Robust ETL processes handle missing values, fix data inconsistencies, normalize sales units, and merge multiple datasets for holistic analysis.

- **Business Insights:** Enables identification of top-performing games and genres, regional market trends, seasonal sales patterns, and publisher performance—supporting data-driven decision making for game developers, publishers, and analysts.

- **User-Friendly Navigation:** Use of bookmarks and navigation buttons enhances the end-user experience by providing quick access to different analytical views, making complex data exploration intuitive.

- **Scalable & Reusable Architecture:** Designed as a blueprint for cloud-based gaming sales analytics dashboards, supporting extensibility to new datasets and analytics requirements.

---

## 📁 Files

- `Video+Games.xlsx`: Raw dataset.
- `Video+Games+Correction+Records.xlsx`: Corrected data
- `Video Games Sales Data Analysis (AWS+Power BI).pbix`: Power BI file including all transformations and visualizations.

---

## 🛠 How to Run the Project

1. Download `Video Games Sales Data Analysis (AWS+Power BI).pbix`.
2. Open the `.pbix` file in Power BI Desktop.
3. Explore the interactive dashboards and uncover insights.

---

## 🤝 Contributions

Suggestions and contributions are welcome! If you have ideas to improve the dashboard or add features, please raise an issue or submit a pull request.
