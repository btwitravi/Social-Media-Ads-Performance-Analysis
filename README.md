# Social Media Ads Performance Analysis

## Project Overview

This project analyzes social media advertising performance using Python to
understand campaign effectiveness across different platforms, campaign types,
industries, countries, and time periods.

The analysis focuses on exploratory data analysis (EDA), data cleaning,
statistical summaries, visualization, performance comparisons, and hypothesis
testing using One-Way ANOVA.

---

## Dataset

The dataset contains **1,800 advertising campaign records** with 14 columns,
including:

- Date
- Platform
- Campaign Type
- Industry
- Country
- Impressions
- Clicks
- CTR
- CPC
- Ad Spend
- Conversions
- CPA
- Revenue
- ROAS

The dataset includes advertising records from multiple platforms, industries,
campaign types, and countries.

---

## Objectives

The main objectives of this project are:

- Understand the structure and quality of the advertising dataset.
- Perform data cleaning and preprocessing.
- Analyze numerical and categorical variables.
- Identify patterns and trends in campaign performance.
- Compare advertising performance across platforms.
- Analyze revenue and ad spend relationships.
- Analyze performance across countries, industries, and campaign types.
- Examine monthly ROAS growth.
- Test whether average ROAS differs significantly across advertising platforms.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

---

## Data Cleaning & Preparation

The dataset was inspected for:

- Data types
- Missing values
- Duplicate records
- Numerical and categorical variables
- Date formatting

The `date` column was converted into datetime format for time-based analysis.

---

## Exploratory Data Analysis

### Numerical Analysis

The project analyzes:

- Impressions
- Clicks
- CTR
- CPC
- Ad Spend
- Conversions
- CPA
- Revenue
- ROAS

Summary statistics such as mean, median, standard deviation, minimum,
maximum, IQR, and skewness were calculated.

The analysis shows that several campaign performance metrics such as clicks,
ad spend, conversions, revenue, and ROAS are right-skewed, with a smaller
number of campaigns producing unusually high values.

---

## Categorical Analysis

The following categorical variables were analyzed:

- Platform
- Campaign Type
- Industry
- Country

### Platform Distribution

- Google Ads: 720 records
- Meta Ads: 630 records
- TikTok Ads: 450 records

### Campaign Type Distribution

- Search: 477
- Video: 456
- Shopping: 447
- Display: 420

The dataset provides reasonably broad representation across platforms,
campaign types, industries, and countries.

---

## Time-Based Analysis

The project analyzes campaign activity and performance across months.

The analysis includes:

- Monthly campaign distribution
- Revenue heatmap by day and month
- Monthly ROAS growth rate

The revenue heatmap indicates variation across different days and months,
while the monthly ROAS analysis shows periods of both positive and negative
growth.

---

## Performance Analysis

### Revenue vs Ad Spend

A scatter plot was used to analyze the relationship between advertising spend
and revenue.

The analysis indicates a positive relationship between ad spend and revenue,
while also showing that higher spending does not always result in proportional
revenue growth.

### Country-Level Analysis

Average revenue and ad spend were compared across countries to understand
regional differences in advertising performance.

### Industry-Level Analysis

Total CPC was compared across industries to examine differences in click
acquisition costs.

### Campaign Type Analysis

Average revenue and ad spend were compared across:

- Search
- Video
- Shopping
- Display

Search campaigns showed the highest average revenue and spending in this
dataset.

---

## Hypothesis Testing

### One-Way ANOVA

The following hypothesis was tested:

**Question:**

> Is there a significant difference in average ROAS between Google Ads,
> Meta Ads, and TikTok Ads?

### Null Hypothesis (H0)

There is no significant difference in average ROAS across Google Ads,
Meta Ads, and TikTok Ads.

### Alternative Hypothesis (H1)

There is a significant difference in average ROAS across at least one of
the platforms.

### Results

| Platform | Mean ROAS |
|---|---:|
| Google Ads | 4.11 |
| Meta Ads | 6.92 |
| TikTok Ads | 9.54 |

**F-statistic:** 107.65

**P-value:** 6.9607e-45

**Significance level:** 0.05

Since the p-value is far below 0.05, the null hypothesis was rejected.

The result provides statistically significant evidence that average ROAS is
not the same across all three advertising platforms.

> Note: ANOVA identifies that at least one platform differs, but it does not
> identify which specific platform pairs are significantly different.
> Pairwise post-hoc testing such as Tukey HSD would be required for that
> analysis.

---

## Key Insights

- Google Ads has the highest number of records in the dataset.
- Campaign types are relatively balanced across Search, Video, Shopping,
  and Display.
- Several numerical performance metrics are positively/right-skewed.
- Ad spend and revenue show a positive relationship.
- Revenue and advertising spend vary across countries.
- CPC varies across industries.
- Campaign performance varies across campaign types.
- Monthly ROAS shows both positive and negative growth periods.
- TikTok Ads has the highest average ROAS in the analyzed dataset.
- One-Way ANOVA indicates a statistically significant difference in average
  ROAS across the advertising platforms.

---

## Project Structure

| File | Description |
|---|---|
| `Social_Media_Ads_Performance.ipynb` | Complete Python analysis and EDA notebook |
| `global_ads_performance_dataset.csv` | Dataset used for the analysis |
| `Social_Media_Ads_Performance_Reports.pdf` | EDA Analysis Reports |
| `README.md` | Project documentation |

---

## Conclusion

This project provides an exploratory and statistical analysis of social media
advertising performance across multiple dimensions.

The analysis combines data cleaning, exploratory data analysis, visualization,
business-oriented comparisons, and hypothesis testing to understand campaign
performance.

The ANOVA results indicate a statistically significant difference in average
ROAS across Google Ads, Meta Ads, and TikTok Ads. However, platform-level
budget decisions should not rely on average ROAS alone and should also
consider factors such as sample size, campaign variation, CPA, conversions,
revenue, and outliers.
