# Website-A-B-Testing

# Introduction

This project analyses A/B test results to compare two versions of a website (Group A vs. Group B) across various metrics, including conversion rates, page views, and time spent. The analysis includes statistical hypothesis testing using multiple approaches to evaluate the effectiveness of the website changes.

# Dataset

The dataset contains the following columns:
- Group: Indicates whether the user was in Group A (control) or Group B (variant).
- Page Views: The number of pages viewed by each user.
- Time Spent: The duration (in minutes) a user spent on the website.
- Conversion: Whether the user made a purchase (Yes/No).
- Device: Whether the user accessed the website via Desktop or Mobile.
- Location: The geographic region (England, Wales, Scotland, or Northern Ireland).

# Installation

- Clone the repostiory using: git clone https://github.com/AdamBartlett7/Website-A-B-Testing.git
- Navigate to the correct directory using: cd Website-A-B-Testing
- Create your own virtual environment with the necessary python libraries using: conda env create -f environment.yml
- Then open and run Website_A_B_Testing.ipynb.

# Usage

- Run Website_A_B_Testing.ipynb in sequential order to see how each test was implemented.

# Project Workflow - Hypothesis Tests Conducted

For this project, I conducted multiple statistical tests to assess differences between Group A and Group B.

# Conversion Rate Analysis

- Chi-Squared Test: Examined whether the conversion rates between Group A and Group B were significantly different.
- Z-Test for Proportions: Compared the conversion rates using a two-proportion Z-test.
- Bayesian A/B Test: Used a Bayesian approach to estimate the probability that one group had a higher conversion rate than the other.

# User Engagement Metrics

- Two-Sample t-Test (Page Views): Tested whether the average number of page views differed between groups.
- Two-Sample t-Test (Time Spent): Evaluated if users in one group spent significantly more time on the website than the other.

# Device Specific Conversion Rate Analysis

- Chi-Squared Test (Desktop Users Only): Analyzed conversion rate differences for desktop users only.
- Chi-Squared Test (Mobile Users Only): Analyzed conversion rate differences for mobile users only.

# Assumption Checking, Sample Size and Power Analysis

- Each test was performed only after verifying that the necessary assumptions were met. Such as independent observations, random assignment of groups, stationarity, normality assumption and more.
- Pre-Test Sample Size Calculation: Prior to each test, I determined the required sample size based on effect sizes, significance level (alpha = 0.05), and desired power (0.8).
- Effect Size Calculation: After conducting each test, I computed the observed effect size (Cohen’s h for proportions, Cohen’s d for t-tests.
- Post-Test Power Analysis: Verified the actual power of each test based on observed sample sizes and effect sizes.

# Results

- Group B had a higher conversion rate than Group A, with statistically significant differences in both the chi-squared test and z-test. But the effect size was only 0.2999. So not very meaningful.
- The Bayesian test indicated a perfect probability that Group B had a higher conversion rate than Group A.
- No significant differences were found in page views or time spent between the two groups.
- When analysing device specific conversions, the difference was significant for both desktop and mobile users. But the effect size for each test were 0.2751 and 0.3255 which again are not particularly high.
- The post test power analysis confirmed that all chi-squared and z-test of proportions had sufficient statistical power. This is due to the sample sizes being much larger than the test required.
  However for the two sample t-test they did not have sufficient statistical power as there samples size were much lower than required.

# Future Imporvements

- Obtain more data for the two sample t-tests, so they have sufficent statistical power.
- Conduct further segmentation analysis such as location.

# License

- This project is licensed under the MIT License. See the LICENSE file for details.


