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

3. How to Use This Repository

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
powerbi/
Open them directly in Power BI Desktop.

4. Key Deliverables
✔ Final Report (APA Format)
sql
Copy code
docs/Capstone-II Final Project Report.docx
✔ Power BI Dashboards
bash
Copy code
powerbi/Capstone_2_Dashboards.pbix
✔ Presentation Deck
sql
Copy code
presentation/Capstone-II Project Final Draft.pptx

5. Analytical Components

5.1 NLP Keyword Analysis

Extracted and cleaned storyline keywords to compute:

Top piracy-driving themes

Keyword-level download correlations

Insert screenshot:
<img width="1939" height="947" alt="Screenshot 2025-11-30 003519" src="https://github.com/user-attachments/assets/971b6004-6a68-4fa4-96b9-5c2149f97e33" />

scss
Copy code


5.2 Piracy Trend Insights
<img width="1941" height="1091" alt="Screenshot 2025-11-30 210945" src="https://github.com/user-attachments/assets/608feb31-b524-406a-8d69-3fdb2d375a22" />
Line chart revealing:

Major piracy spikes (2013–2017)

Drops during the rise of streaming platforms

Recovery in 2021–2023

Insert screenshot:

scss
Copy code


5.3 Genre Insights
<img width="1941" height="1088" alt="Screenshot 2025-11-30 213150" src="https://github.com/user-attachments/assets/aa952fd4-6cdb-42eb-bfc9-5f21fa9bee39" />
Analyzed:

Average Budget per Genre
<img width="1941" height="1088" alt="Screenshot 2025-11-30 213150" src="https://github.com/user-attachments/assets/c70e210d-2325-418b-bf73-3a61f823b4b5" />

User Rating Patterns
<img width="1932" height="1096" alt="Screenshot 2025-11-29 222432" src="https://github.com/user-attachments/assets/02b491a0-c198-40d2-b491-6dace181441d" />

Genre frequency
<img width="1941" height="1091" alt="Screenshot 2025-11-30 210945" src="https://github.com/user-attachments/assets/608feb31-b524-406a-8d69-3fdb2d375a22" />
Download behavior by category
<img width="1940" height="1092" alt="Screenshot 2025-11-30 002456" src="https://github.com/user-attachments/assets/43eac232-289b-40cf-ba25-7e7a0ae44f44" />

5.4 Revenue & Budget Analysis
<img width="1940" height="1090" alt="Screenshot 2025-11-30 004335 - Copy" src="https://github.com/user-attachments/assets/2ea1937a-e73a-4280-9783-4be223b56e70" />

Includes:

Top 20 Highest-Grossing Films
<img width="1947" height="1091" alt="Screenshot 2025-11-30 230424" src="https://github.com/user-attachments/assets/320bca1c-19fd-4d77-8f83-f66eca81378b" />

Top 20 Most Pirated Movies
<img width="1941" height="885" alt="Screenshot 2025-11-30 001126" src="https://github.com/user-attachments/assets/5c2b5a55-2796-449d-869d-288e4316a771" />

Budget vs Downloads scatter
<img width="1944" height="1085" alt="Screenshot 2025-11-30 211606 - Copy" src="https://github.com/user-attachments/assets/c24eea93-be46-4949-bab5-fd182e27e58d" />

ROI patterns
<img width="1941" height="1088" alt="Screenshot 2025-11-30 213150" src="https://github.com/user-attachments/assets/b7c3ab79-98f0-4fd4-b895-0a1931476628" />

<img width="1940" height="1090" alt="Screenshot 2025-11-30 004335 - Copy" src="https://github.com/user-attachments/assets/d6f4b85b-5535-4cbd-8437-2730ea98f827" />



5.5 Storyline Length vs Downloads

Studied how storyline complexity impacts piracy.

Key finding:

Short, high-concept plot summaries show higher piracy engagement.

<img width="1940" height="1090" alt="Screenshot 2025-11-30 002957 - Copy" src="https://github.com/user-attachments/assets/24b18c9b-a761-4650-a1d8-1f620eee4359" />


<img width="1943" height="1091" alt="Screenshot 2025-12-01 221156" src="https://github.com/user-attachments/assets/873fd444-84d1-4549-b09d-073349f5fbce" />

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
