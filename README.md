# Capstone-2-Movie-Piracy-Analytics
From Script to Screen: Predicting Movie Success with Analytics &amp; Piracy Insights (Power BI + NLP + Piracy Analytics)


# **From Script to Screen: Predicting Movie Success With Analytics & Piracy Insights**  
### *(Power BI + Python + NLP + BigQuery + TMDb/Kaggle Data)*

---

##  **1. Project Overview**

This repository contains the full analytics workflow for the Capstone II project:  
**From Script to Screen — Predicting Movie Success with Analytics & Piracy Insights.**

The project analyzes:

- Piracy trends  
- Genre behavior  
- Movie success factors  
- NLP-based storyline keyword patterns  
- Budget–revenue–downloads relationships  

Using:

- **Power BI Dashboards**  
- **Python ETL + NLP**  
- **BigQuery SQL**  
- **TMDb & Kaggle datasets**

The repository includes the final report, PPT deck, processed datasets, scripts, and reusable files for reproducible analytics.

---

## **2. Repository Structure**

```text
capstone2-movie-piracy-analytics/
├── data_raw/                     # Original CSVs (excluded via .gitignore)
├── data_processed/               # Cleaned & enriched datasets
├── docs/                         # Final report, documentation
├── images/                       # Dashboard screenshots for README + PPT
├── powerbi/                      # PBIX files + Power BI exports
├── presentation/                 # Final PPT deck
├── scripts/                      # Python ETL, NLP, preprocessing code
├── .gitignore
└── README.md
```
## ** 3. How to Use This Repository **

Clone the project

bash
Copy code

git clone https://github.com/madhukargoli1992G/capstone2-movie-piracy-analytics.git

cd capstone2-movie-piracy-analytics
Install Python dependencies

bash
Copy code

pip install -r requirements.txt
Open Power BI dashboards
All .pbix files are located in:

Copy code

PowerBI/Capstone_2_Dashboards.pbix
Open them directly in Power BI Desktop.

4. Key Deliverables
   
✔ Final Report (APA Format)

docs/Capstone-II Final Project Report.docx
✔ Power BI Dashboards

powerbi/Capstone_2_Dashboards.pbix

✔ Presentation Deck

presentation/Capstone-II Project Final Draft.pptx

## ** Power BI Data Model **

![Power BI Data Model](Images/Screenshot%202025-11-29%20221157.png)
The analytical backbone of this project is a relational data model built in Power BI, designed to unify metadata, ratings, piracy activity, storyline keywords, and extended film attributes into a single analytical framework.

This model ensures clean relationships across datasets, enabling accurate DAX calculations, cross-filtering, and integrated insights across the dashboards.

## ** Key Components of the Data Model **

1. movies_metadata (Central Fact Table)

Contains core attributes for each movie:

id (primary identifier)

MovieKey

budget, revenue, profit

popularity, imdb_id, homepage

genres, Genre_Category, Genre_Category_Family

release_date, original_language

Supports relationships to ratings, piracy, keywords, and credits.

2. movies_dataset (Piracy & Extended Attributes)

Includes:

downloads (Total piracy downloads)

storyline, run_time, posted_date, release_date

industry, appropriate_for, writer, director

Linked using MovieKey.

3. ratings_small

Provides:

movieId, rating, timestamp

Enables creation of average IMDB-style rating metrics.

4. credits

Includes cast/crew information:

cast, crew, id

Supports segmentation of piracy by genre family and rating category.

5. keywords_explored (NLP Model Output)

Stores keyword occurrences extracted from storyline text:

KEYWORD

Total Downloads Keyword

Provides inputs for the NLP Word Cloud and the Top Keyword Frequency visual.

5. Analytical Components

5.1 NLP Keyword Analysis

Extracted and cleaned storyline keywords to compute:

![NLP Piracy Keywords](Images/Screenshot%202025-12-01%20215934.png)

Top piracy-driving themes

Keyword-level download correlations

## ** Dataset OverView Dashboard **

![DATASET OVERVIEW](Images/Screenshot%202025-11-29%20222252.png)

5.2 Piracy Trend Insights

![Piracy Line Chart ](Images/Screenshot%202025-11-30%20210945.png)

Line chart revealing:

Major piracy spikes (2013–2017)

Drops during the rise of streaming platforms

Recovery in 2021–2023

5.3 Genre Insights

![Genre Insights](Images/Screenshot%202025-11-30%20004335%20-%20Copy.png)

Analyzed:

Average Budget per Genre
![AVG BUDGET PER GENRE](Images/Screenshot%202025-11-30%20213150.png)

User Rating Patterns
![USER RATINGS](Images/Screenshot%202025-11-29%20223836.png)

Genre Vs Piracy
![Ratings vs Piracy by Genre](Images/Screenshot%202025-11-29%20232731.png)

5.4 Revenue & Budget Analysis

Includes:

Top 20 Highest-Grossing Films

![TOP 20 Highest Grossing Movies](Images/Screenshot%202025-11-30%20230424-%220Copy.png)

Top 20 Most Pirated Movies

![Top 20 Most Pirated Movies](Images/Screenshot%202025-11-30%20001126.png)

Budget vs Downloads scatter

![Budget vs Downloads](images/Screenshot%202025-11-30%20211606.png)

ROI patterns

![ROI](Images/Screenshot%202025-11-30%20004335-%20Copy.png)

![ROI](Images/Screenshot%202025-12-01%20220519.png)

5.5 Storyline Length vs Downloads

![Storyline Length vs Downloads](Images/Screenshot%202025-12-01%20221156.png)

Studied how storyline complexity impacts piracy.

Key finding:

Short, high-concept plot summaries show higher piracy engagement.

6. Core Findings

✔ High piracy clusters appear in action, thriller, and high-concept films
✔ Story keywords strongly predict piracy behavior
✔ Large budgets do not guarantee popularity — many low-cost films perform well
✔ Ratings concentrate around 6–7 but piracy distribution differs
✔ Industry-level differences show Hollywood dominating budgets and downloads

7. Reproducibility Guide

Run all preprocessing scripts
bash
Copy code
python scripts/preprocess_keywords.py
python scripts/clean_dataset.py
Rebuild dashboards
Open Power BI

Load processed datasets

Refresh queries

Reconnect relationships as needed

8. Large Files Policy

Raw files such as:

credits.csv

Credits_Calculated_Cleaned.csv

are excluded via .gitignore due to GitHub size limits.

They can be downloaded separately from TMDb/Kaggle.

9. Team Members (Group X)
Madhukar Goli — Data Engineer, Visualization Lead

(Add additional group members if applicable)

10. References (APA Format)
TMDb API. (2024). The Movie Database (TMDb) API documentation. https://developer.themoviedb.org/

Kaggle. (2024). The Movies Dataset. https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset

Microsoft. (2024). Power BI documentation. https://learn.microsoft.com/power-bi/

Danaher, B., Smith, M., Telang, R., & Chen, S. (2014). The effect of piracy on sales of media goods: A retrospective. Journal of Industrial Economics.

11. Acknowledgements
Project completed for:

MSBA 286 — Capstone Project II
Eberhardt School of Business, University of the Pacific

12. License
This repository is for academic use only.
Redistribution or commercial use of raw datasets is prohibited.
