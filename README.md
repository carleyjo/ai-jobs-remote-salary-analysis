# ai-jobs-remote-salary-analysis
This project investigates how remote work status relates to salaries in AI and data science roles. As I pursue my Master’s degree in Data Science at the University of St. Thomas, understanding potential salary differences between fully remote and hybrid roles is especially relevant as I evaluate my long-term career goals.

## Project Scaffold Table

| Element | My Plan |
|--------|-----------|
| **Topic / Question** | Do fully remote AI and data science jobs pay higher salaries than non-remote or hybrid roles? |
| **Hypothesis** | Fully remote AI and data science jobs have a higher median salary than non-remote or hybrid roles. |
| **Outcome / Metric / Test Statistic** | Salary in USD (`salary_in_usd`); difference in median salary between fully remote and non-remote/hybrid roles; permutation test. |
| **Units of Analysis** | Each observation represents a single AI or data-related job record. |
| **Data Source(s)** | `salaries-ai-jobs-net.csv` from the Plotly public datasets repository: https://github.com/plotly/datasets/blob/master/salaries-ai-jobs-net.csv |
| **Why this data works** | The dataset includes standardized salary data and a clear measure of remote work status, allowing for direct comparison of compensation across work arrangements. |
| **Uncertainty Metric** | Bootstrap confidence interval for the median salary of fully remote roles. |
| **Null Hypothesis** | There is no difference in median salary between fully remote and non-remote or hybrid AI/data science jobs. |