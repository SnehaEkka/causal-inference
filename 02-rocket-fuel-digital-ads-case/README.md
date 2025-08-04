# Rocket Fuel Digital Ads Effectiveness Case

## Overview

This exercise investigates causal inference through a real-world, large-scale digital advertising experiment conducted for TaskaBella by Rocket Fuel. The notebook walks through the end-to-end measurement of campaign effectiveness and profitability using the “lift” from randomized ad exposure, coupled with robust statistical interpretation and visualization.

## Tools Used
- **Python 3.x**
- **Jupyter/IPython Notebook**
- **pandas** (data manipulation)
- **NumPy** (numerical analysis)
- **seaborn/matplotlib** (data visualization)
- **statsmodels** (statistical tests)
- **pingouin** (power analysis)

## Business Objective

**Key Questions:**
- Did showing digital ads convert more customers, and was this increase statistically significant?
- Was the ad campaign profitable for TaskaBella?
- How does ad exposure (impressions, times, days) influence conversion rates and campaign ROI?
- How should future digital ad experiments be designed for maximum insight and efficiency?

**Purpose:**  
This case study provides an applied blueprint for marketers and analysts, illustrating how experiments can demonstrate and quantify the causal impact of advertising on sales, empower budget decisions, and refine campaign design.

## Dataset Structure

Each row represents a unique user in the ad campaign, with the following columns:
- **user_id:** Unique user identifier.
- **test:** 1 if exposed to the real ad, 0 if shown a public service announcement (PSA/control).
- **converted:** 1 if the user bought the product, 0 otherwise.
- **tot_impr:** Total number of times the user saw the ad or PSA.
- **mode_impr_day:** Day of week with most impressions (1=Monday, …, 7=Sunday).
- **mode_impr_hour:** Hour of day with most impressions (0-23).

## Exercise Structure & Analysis

### 1. Ad Effectiveness & Causal Impact
- **ATE Estimation:** Compute and interpret the Average Treatment Effect (ATE), the causal “lift”, by comparing conversion rates in treatment vs. control.
- **Statistical Significance:** Use t-tests to assess if the observed difference could be due to chance.
- **Practical Interpretation:** Translate statistical outcomes (ATE, p-values, t-scores) into plain language business conclusions.

### 2. Profitability & ROI
- **Campaign Profit Calculation:** Quantify incremental profit (conversions x margin) due to ads.
- **Cost Calculation:** Compute total campaign cost by impressions served.
- **ROI Analysis:** Assess overall efficiency and profitability of the campaign using standard ROI metrics.
- **Opportunity Cost:** Evaluate the financial impact of allocating users to control versus exposing everyone to advertising.

### 3. Impressions & Conversion Dynamics
- **Dose-Response:** Analyze and visualize how conversion rates change with the number of ad exposures (binned).
- **Business Implication:** Discuss regions of greatest advertising impact to guide future frequency capping and audience targeting.

### 4. Power, Effect Size, & Experimental Design
- **Effect Size (Cohen’s D):** Quantify the magnitude of the campaign lift.
- **Power Calculations:** Use sample size and effect size to gauge the study's ability to detect true effects.
- **Experimental Recommendations:** Advise on control group sizing and power for future studies.

### 5. Presentation & Business Communication
- **Managerial Summary:** Synthesize findings into concise, actionable recommendations for TaskaBella management.

## Key Insights & Results

- **Causal Impact Detected:** The ad campaign produced a small but statistically significant lift in conversions.
- **Positive ROI:** TaskaBella’s campaign was profitable, achieving a 32% return after costs.
- **Optimal Impression Range:** Conversion rates increased with exposure, plateauing after a certain number of impressions, optimal for frequency planning.
- **Experimental Power:** High sample size delivered near-certain power to detect even modest campaign effects.
- **Design Recommendations:** Proper control group sizing and power analysis are vital for meaningful, actionable conclusions in digital ad testing.

## How to Run / Use

1. Download the IPython notebook (`BA830-Ex-2-Rocket-Fuel-Case.ipynb`) and the dataset (`rocketfuel_data.csv`).
2. Open the notebook in Jupyter Lab/Notebook or your chosen coding environment.
3. Run code blocks sequentially to reproduce the analysis, charts, and managerial recommendations.

## Requirements

- Python ≥ 3.7  
- pandas, numpy, seaborn/matplotlib  
- statsmodels, pingouin

## Learning & Takeaways

- Applied causal inference to a real-world business experiment.
- Quantified both statistical and practical business outcomes of a randomized digital ad campaign.
- Developed skills in power analysis and effect size interpretation for experimental design.
- Practiced communicating data-driven recommendations directly to business stakeholders.

## Project Details

- **Completed:** February 2024  
- **Course:** Business Experimentation & Causal Methods (BA830), Boston University MSBA

*This exercise shows how carefully designed experiments and rigorous analysis can extract causal business insights, driving smarter digital marketing and advertising decisions.*
