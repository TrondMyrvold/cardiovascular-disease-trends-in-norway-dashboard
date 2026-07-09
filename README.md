# Cardiovascular Disease Trends in Norway (2021–2025)

## Project Overview

This project was created to further improve my skills in Power BI, DAX, and interactive dashboard development using real-world healthcare data.

The objective was to explore trends in cardiovascular disease diagnoses in Norway between 2021 and 2025 using publicly available data from the Norwegian Institute of Public Health (FHI).

The project focused on transforming raw public health data into an interactive dashboard capable of identifying diagnosis trends, yearly changes, and long-term developments through dynamic visualizations and DAX calculations.

---

# Project Objectives

The objectives of this project were to:

- Explore trends in cardiovascular disease diagnoses between 2021 and 2025.
- Identify the most common cardiovascular diagnoses.
- Compare annual patient counts across diagnosis groups.
- Calculate year-over-year changes using DAX.
- Build an interactive Power BI dashboard for healthcare data exploration.

---

# Dataset

- **Source:** Norwegian Institute of Public Health (FHI) https://statistikk.fhi.no/
- **Format:** Excel (.xlsx)
- **Data Type:** Public healthcare statistics

The dataset contains yearly counts of registered cardiovascular disease diagnoses in Norway between 2021 and 2025.

The dashboard allows users to explore trends for individual diagnosis groups while comparing changes over time.

---

# Data Cleaning

The original dataset required minor preprocessing before visualization.

The data preparation process included: 

- Removing unnecessary metadata
- Renaming and cleaning columns
- Preparing the dataset for Power BI analysis

---

# Dashboard

An interactive Power BI dashboard was created to analyze cardiovascular disease diagnoses.

# Dashboard Features

- Interactive Year and Diagnosis slicers
- Dynamic KPI cards
- Year-over-year calculations
- Heatmap matrix with conditional formatting
- Diagnosis ranking
- Treemap visualization
- Interactive trend analysis

Users can:

- Filter by diagnosis group
- Filter by year
- Compare yearly patient trends
- Explore diagnosis rankings
- View diagnosis distribution
- Compare annual percentage changes
- View dynamic KPI cards

![Dashboard](Images/dashboard.png)

---

# What the data shows us

## Diagnosis Trends

Between 2021 and 2025, the overall number of registered cardiovascular disease patients remained relatively stable. While the total disease burden changed only modestly, individual diagnosis groups followed different trajectories over the five-year period.

Hypertension (I10–I15) consistently remained the most common cardiovascular diagnosis throughout the study period, accounting for the largest patient population every year. Atrial fibrillation and ischemic heart disease also represented a substantial proportion of registered diagnoses and remained among the most prevalent conditions.


## Changes Over Time

Although the overall patient population only changed gradually, the dashboard reveals noticeable differences between the diagnosis groups.

Heart failure was the diagnosis group that showed the strongest relative increase during the study period, growing by approximately 16.8% between 2021 and 2025. Hypertension also had a steady growth, while atrial fibrillation showed a moderate upward trend.

In contrast, ischemic heart disease gradually declined across the study period, suggesting a reduction in registered patients for this diagnosis. Several acute cardiovascular conditions, including acute myocardial infarction and acute stroke, changed only slightly from year to year and remained comparatively stable.

The matrix highlights yearly changes in the diagnosis groups, and all of them shows relatively small annual changes, typically only a few percentage points between consecutive years. This indicates that cardiovascular disease patterns in Norway changed gradually rather than through sudden shifts.

# Overall Story

The dashboard illustrates that cardiovascular disease remains a stable public health challenge in Norway. Rather than dramatic increases in total patient numbers, the most interesting findings are the changing composition of diagnoses over time.

Chronic conditions such as hypertension and heart failure became increasingly prominent during the five-year period, while ischemic heart disease showed a gradual decline. These contrasting trends demonstrate how disease patterns can evolve even when the overall number of patients remains relatively constant.

## Feature Engineering

Several DAX measures were created to improve dashboard interactivity.

Measures include:

- Total Patients
- Previous Year Patients
- Yearly Change
- Growth %
- Most Common Diagnosis
- Fastest Growing Diagnosis
- Largest Increase %

These measures update dynamically based on the selected diagnosis group and year.

---

# Tools Used

- Power BI Desktop
- Power Query
- DAX
- Microsoft Excel
- Data Cleaning
- Data Visualization

---

# Key Findings

- Hypertension (I10–I15) remained the most common cardiovascular diagnosis throughout the study period.
- Overall patient volumes remained relatively stable between 2021 and 2025.
- Heart failure experienced the highest relative growth among the diagnosis groups.
- Most diagnosis groups showed only modest year-over-year variation.

---

# Learning Outcomes

Through this project I improved my experience with:

- Power BI
- DAX
- Power Query
- Interactive Dashboard Design
- KPI Development
- Healthcare Data Analysis
- Data Storytelling
- Working with real-world public healthcare datasets

---

# Disclaimer

This project was created as part of my learning journey in Data Analytics.

The primary objective was to practice Power BI, DAX, dashboard design, and interactive data visualization using publicly available healthcare data from the Norwegian Institute of Public Health (FHI).

The dashboard was developed for educational and portfolio purposes and should not be interpreted as an official healthcare analysis.
