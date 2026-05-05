# Data

The dataset used in this project is not stored directly in the GitHub repository.

## Dataset
- **File name:** salaries-ai-jobs-net.csv
- **Source:** Plotly public datasets repository
- **URL:** https://github.com/plotly/datasets/blob/master/salaries-ai-jobs-net.csv

## Unit of Analysis
Each row represents a single AI or data-related job record, including salary information, job title, experience level, company characteristics, and remote work status.

## Key Variables
- `salary_in_usd`: Annual salary converted to U.S. dollars; primary outcome variable.
- `remote_ratio`: Percentage of time worked remotely (0 = on-site, 50 = hybrid, 100 = fully remote); main explanatory variable.
- `experience_level`: Seniority level of the role; potential confounding variable.
- `job_title`: Job role title; useful for interpreting salary variation.
- `company_size`: Size of the employer; contextual variable related to compensation.

## Variable Definitions
- `work_year`: Year the salary information was reported.
- `experience_level`: Seniority level of the role (EN = Entry-level, MI = Mid-level, SE = Senior-level, EX = Executive-level).
- `employment_type`: Type of employment contract (FT = Full-time, PT = Part-time, CT = Contract, FL = Freelance).
- `job_title`: Job role title (e.g., Data Analyst, Data Scientist, AI Scientist).
- `salary`: Reported salary in the original currency.
- `salary_currency`: Currency in which the salary was paid.
- `salary_in_usd`: Salary converted to U.S. dollars.
- `employee_residence`: Country where the employee resides.
- `remote_ratio`: Percentage of time worked remotely (0 = on-site, 50 = hybrid, 100 = fully remote).
- `company_location`: Country where the employer is located.
- `company_size`: Size of the employer (S = Small, M = Medium, L = Large).

## Reproducibility
To reproduce this analysis:
1. Download the dataset from the URL above
2. Save the file as `salaries-ai-jobs-net.csv`
3. Place the file inside this `data/` directory