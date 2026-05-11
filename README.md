# ai-jobs-remote-salary-analysis

This project examines how remote work status relates to salaries in AI and data science roles. As I pursue my Master’s degree in Data Science at the University of St. Thomas, understanding potential compensation differences between fully remote, hybrid, and on-site roles is directly relevant as I evaluate my long-term career goals.

In addition to personal career insights, this analysis is grounded in advancing the common good by exploring whether salary disparities exist that could disadvantage individuals who rely on remote work due to accessibility, health, caregiving, or geographic constraints. By identifying and highlighting any such patterns, the project aims to support more equitable and inclusive workplace practices within the data science field.

---

## 1. Research Question

Do fully remote AI and data science jobs pay higher salaries than non-remote or hybrid roles?

---

## 2. Data

The analysis uses the `salaries-ai-jobs-net.csv` dataset from the Plotly public datasets repository. Each observation represents a single AI or data-related job record and includes salary information, job characteristics, company attributes, and remote work status.

Salary values are standardized using the `salary_in_usd` variable, allowing for comparison across countries and currencies. Remote work status is captured using `remote_ratio`, which indicates whether a role is on-site (0), hybrid (50), or fully remote (100). Only full-time roles are included in the final analysis.

The dataset is not stored directly in this repository. Instructions for downloading and placing the data locally are provided in the `data/` folder.

---

## 3. Hypothesis and Methodology

This project follows the *Only One Test* framework.

The test statistic is the difference in **median salary (USD)** between fully remote roles and non-remote or hybrid roles. Median salary is used rather than the mean because salary distributions are strongly right-skewed and contain extreme outliers.

- **Null hypothesis (H₀):**  
  There is no difference in median salaries between fully remote AI/data science jobs and non-remote or hybrid jobs.

- **Alternative hypothesis (H₁):**  
  Fully remote AI/data science jobs have a higher median salary than non-remote or hybrid jobs.

A permutation test is used to evaluate the hypothesis, as it does not rely on distributional assumptions and is appropriate for skewed data.

---

## 4. Exploratory Data Analysis

Exploratory data analysis was conducted to understand the structure of the dataset, assess salary distributions, and examine differences by remote work status.

Salary distributions are strongly right-skewed, with most salaries clustered below $150,000 and a small number of high earners extending the upper tail. Descriptive statistics show that the mean salary exceeds the median, reinforcing the decision to focus on medians for comparison.

Boxplots comparing salaries by remote work status indicate that fully remote roles tend to have higher median salaries and greater variability than on-site and hybrid roles. Hybrid roles consistently show the lowest typical compensation.

---

## 5. Results

The observed test statistic—the difference in median salary between fully remote roles and non-remote or hybrid roles—was approximately **$32,329**.

A permutation test with 5,000 resamples produced a p-value smaller than **0.001**, indicating that the observed difference in median salaries is extremely unlikely to have occurred under the null hypothesis of no difference. This provides strong evidence that remote work status is associated with salary differences in AI and data science roles.

Bootstrap confidence intervals further support this finding. The 95% bootstrap confidence interval for the median salary of fully remote roles ranges from approximately **$110,000 to $128,875**. The 95% bootstrap confidence interval for the difference in median salaries between fully remote and non-remote or hybrid roles ranges from about **$19,680 to $44,926**.

---

## 6. Uncertainty Estimation

Uncertainty was estimated using bootstrap resampling with **5,000 resamples** for each metric. Bootstrap distributions for both the median salary of fully remote roles and the difference in median salaries were right-skewed but tightly concentrated around positive values.

The Central Limit Theorem does not apply because the statistic of interest is the median rather than the mean and because salary data are highly skewed. Bootstrap confidence intervals therefore provide an appropriate and interpretable measure of uncertainty. The resulting intervals suggest that the salary advantage observed for fully remote roles is both statistically and practically meaningful.

---

## 7. Limitations

This analysis is observational and does not establish a causal relationship between remote work status and salary. Factors such as job title, experience level, geographic cost of living, and company compensation policies were not controlled for and may partially explain observed differences.

Additionally, the dataset contains more fully remote roles than hybrid or on-site roles, reflecting current labor market patterns but potentially affecting variability and the presence of outliers. Salary data are self-reported, which may introduce reporting bias or measurement error.

---

## 8. References

- Plotly Public Datasets Repository. *AI Jobs Salary Dataset.*  
  https://github.com/plotly/datasets/blob/master/salaries-ai-jobs-net.csv