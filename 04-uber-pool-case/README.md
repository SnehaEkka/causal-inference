# Uber POOL Case: Causal Inference & Platform Field Experimentation

## Overview

This exercise applies statistical analysis and causal inference to a real-world platform experiment at Uber, focusing on the launch and field testing of Express POOL versus the classic Uber POOL service. You will use an authentic operational dataset from Uber's 2018 Boston experiment to investigate the business and behavioral tradeoffs influenced by wait times in a ride-sharing market.

## Case Summary (Relevant to This Exercise)

“Innovation at Uber: The Launch of Express POOL” (HBS) profiles Uber’s experimental rollout of Express POOL—a service designed to improve ride-matching efficiency by asking riders to (a) walk a short distance to set pick-up/drop-off points, and (b) wait briefly before being matched for a cheaper ride. 

Uber piloted Express POOL in Boston and San Francisco and then ran a structured "switchback" experiment in Boston, alternately setting the wait time to 2 minutes (control) or 5 minutes (treatment).  
Management and data scientists weighed the trade-offs: **Longer waits reduced costs but increased rider cancellations**. Balancing customer experience, cost efficiency, and data integrity, Uber used randomized experimentation and causal measurement to guide these critical platform decisions.

## Tools Used
- **Python 3.x**
- **Jupyter/IPython Notebook**
- **pandas** (data processing)
- **NumPy** (numerical/statistical computation)
- **statsmodels/pyfixest** (regression & causal inference)
- **matplotlib**, **seaborn**, **plotnine** (visualization)
- **stargazer** (regression table formatting)

## Business/Platform Objective

**Key Questions:**
- How does changing wait time (from 2 to 5 minutes) affect business outcomes like cancellations, efficiency, total profit, and customer willingness to use shared rides?
- Can randomized field experiments and regression methods quantify these effects reliably in a fast-moving tech environment?
- How should Uber design experiments to support actionable, generalizable insights?

**Purpose:**  
This exercise helps develop expertise in using data engineering and regression analysis for causal inference, platform optimization, and business decision-making in digital marketplaces.  

## Dataset Description

*File: `wait_time_switchback_3.csv`*

- Each observation: a timeblock in the Boston Uber market, randomized to either short (2 min) or long (5 min) wait before batching riders (“switchback” design)
- Key columns:
    - `treat`: 1 if 5-min wait, 0 if 2-min control
    - `wait_time`: “2 mins” or “5 mins”
    - `trips_pool`: classic UberPOOL ride count
    - `trips_express_pool`: Express POOL ride count
    - `rider_cancellations`: number of riders who canceled
    - `total_driver_payout_sr`: sum Uber paid drivers for these trips
    - `revenue`: the sum riders were charged
    - Time variables: period, commute indicator
- *See the file for full column details.*

## Exercise Structure & Analysis

1. **Experimental Design**
   - Understand Uber’s switchback setup and why separating treatment blocks over time (not just users) helps address platform network effects.

2. **Data Engineering**
   - Compute *total_trips = trips_pool + trips_express_pool*.
   - Compute *profit = revenue - total_driver_payout_sr*.
   - Optional: create features like "profit per trip," "share of express pool," and time-of-day effects.

3. **Descriptive & Graphical Analysis**
   - Summarize and visualize treatment vs. control for outcomes (e.g., mean cancellations, profit, total trips).
   - Plot distributions and time series to spot patterns and a balance test.

4. **Regression & Causal Inference**
   - Use OLS regression (or pyfixest) to estimate the treatment effect of a 5-minute wait on:
      - *Profit*, *cancellations*, *number of trips*
      - Control for time of day if needed to account for rush-hour effects
   - Optionally, explore heterogeneity by commute period or baseline ride volume.

5. **Interpretation**
   - Quantify the business tradeoffs: when does increased efficiency outweigh customer inconvenience?
   - What insights should Uber management draw about scaling wait-time changes across the platform?

## Key Insights & Results

- **Causal Impact:**
    - Longer wait times generally increase matching efficiency and platform profit, but may alienate riders.
    - Uber must balance short-term economic gains with long-term customer loyalty and competitive risk.
- **Field Experimentation:**
    - "Switchbacks" help control for time-varying confounders when testing operational tweaks.
    - Data-driven decisions integral to high-growth tech product management.
- **Strategic Application:**
    - Results inform not just Uber’s design, but experimentation best practices for digital platforms more broadly.

## How to Use / Run

1. Download `BA830_Ex_4_Uber_POOL_Case.ipynb` and `wait_time_switchback_3.csv`.
2. Place both files in the same folder (recommended folder name: `04-uber-pool-case`).
3. Open the notebook in Jupyter Lab/Notebook or your favorite platform.
4. Step through the cells to run data engineering, analysis, and regression.
5. Review, interpret, and answer all questions directly in the notebook.

## Requirements

- Python ≥ 3.7
- pandas, numpy, matplotlib, seaborn, statsmodels, or pyfixest (see requirements.txt)

## Learning & Takeaways

- Apply experimentation analysis and regression to platform product data.
- Practice causal inference and data engineering for field experiment evaluation.
- Develop actionable business recommendations from real experiment results.

## Project Details

- Completed: Spring 2024
- Course: Business Experimentation & Causal Methods (BA830), Boston University MSBA
- This exercise demonstrates platform experimentation, causal analysis, and data-driven product strategy in a real-world tech context.

*Based on Harvard Business School case "Innovation at Uber: The Launch of Express POOL" (2018).*
