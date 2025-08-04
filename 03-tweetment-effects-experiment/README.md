# Tweetment Effects on the Tweeted

## Social Media Field Experiment Analysis

## Overview

This exercise uses regression analysis to explore results from a pioneering social media field experiment, inspired by the paper ["Tweetment Effects on the Tweeted: Experimentally Reducing Racist Harassment"](https://link.springer.com/article/10.1007/s11109-016-9373-5) by Kevin Munger. The study investigates whether targeted, randomized responses to racist tweets can affect future online behavior, with outcomes measured using changes in users’ subsequent tweet content.

### Paper Summary (Relevant to This Exercise)

Munger (2017) conducted a large-scale field experiment on Twitter to understand whether confronting accounts posting racist content can reduce subsequent racist expression. Accounts identified as posting racist tweets were randomly assigned to receive a reply from a newly created account (with varying characteristics—number of followers and racial in-group/out-group status), or to a control group receiving no reply. The responses were standardized messages calling out the racist content. Behavior following the intervention was tracked and quantified ("racism scores") using text analysis over one and two months. The paper provides a unique example of using randomized digital interventions and regression to study social and behavioral change online, which this exercise closely mirrors.

## Tools Used
- **Python 3.x**
- **Jupyter/IPython Notebook**
- **pandas** (data manipulation)
- **NumPy** (numerical/statistical computation)
- **statsmodels** or **scikit-learn** (regression analysis)
- **matplotlib/seaborn** (data visualization)

## Business/Social Science Objective

**Key Questions:**
- Does directly confronting racist content on social media reduce subsequent racist behavior among users?
- Which characteristics of the intervention (in-group vs. out-group responder, follower count) drive the strongest effects?
- How can randomized field experiments and regression methods quantify causal impacts in online environments?

**Purpose:**  
The analysis provides practical and theoretical insight into causal inference on digital platforms, showing how social interventions can be tested—and their impacts measured—using modern experimentation and statistical tools.

## Dataset Description

Each observation represents a Twitter account previously flagged for racist content and randomized into a study group. Key variables include:

| Variable                    | Description                                                                                 |
|-----------------------------|--------------------------------------------------------------------------------------------|
| `treatment_arm`             | Group assignment: 0 (control) or treatments 1–4 (varying responder characteristics)        |
| `any_treatment`             | 1 if assigned to any treatment, 0 if control                                               |
| `anonymity`                 | How anonymous the account was (0=least, 2=most)                                           |
| `log.followers`             | Log-transformed follower count of the responding account                                   |
| `racism.scores.pre.2mon`    | Pre-experiment racism score (2 months prior)                                               |
| `racism.scores.post.2mon`   | Post-experiment racism score (2 months after)                                              |
| `racism.scores.post.1mon`   | Post-experiment racism score (1 month after)                                               |

*(See `tweetment_effect.csv` for full details.)*

## Exercise Structure & Analysis

### 1. Experimental Design
- Accounts posting racist tweets were randomized to receive a confronting reply (one of four arms) or no reply (control).
- Treatment arms varied responders’ in-group/out-group status and their follower count (status).
- The primary outcome is change in racism scores post-treatment, controlling for baseline behavior.

### 2. Data Exploration & Regression Analysis
- Summarize and visualize sample characteristics.
- Check for covariate balance and baseline differences between groups.
- Model outcome variables using OLS regression:
    - Regress post-treatment racism scores on treatment indicators, controlling for covariates.
    - Investigate heterogeneity by arm, anonymity, and follower effects.
- Interpret regression output in plain language, focusing on statistical and substantive significance.

### 3. Causal Inference & Business/Social Impact
- Quantify the average treatment effect of receiving a confronting reply.
- Discuss which intervention characteristics (e.g., peer status, group identity) most effectively reduce racist tweeting.
- Connect quantitative results to policy and platform content moderation strategies.

## Key Insights & Results

- **Causal Impact**: Evidence is evaluated for whether confronting racist tweets reduces measured racist behavior, and which types of responses are most effective.
- **Mechanisms & Heterogeneity**: Analysis explores the role of anonymity, baseline racism, and responder characteristics in moderating treatment effects.
- **Social Science Application**: Demonstrates the power and limitations of field experiments and regression for evaluating online interventions.

## How to Use / Run

1. Download the IPython notebook (`BA830-Ex-3-Tweetment-Effect.ipynb`) and the dataset (`tweetment_effect.csv`).
2. Place both files in the same directory (ensure any referenced images, such as `treatment_arms.jpg`, etc, are also present if needed for completeness).
3. Open and run the notebook in Jupyter Lab/Notebook or your preferred coding/cloud environment.
4. Follow the step-by-step workflow to replicate the full analysis.

## Requirements

- Python ≥ 3.7  
- pandas, numpy, matplotlib, seaborn  
- statsmodels or scikit-learn for regression

## Learning & Takeaways

- Apply regression and causal inference to field experimental data.
- Practice modern techniques for analyzing randomized trials in digital/social media contexts.
- Critically interpret empirical results and connect to real-world social impact.

## Project Details

- **Completed:** Spring 2024  
- **Course:** Business Experimentation & Causal Methods (BA830), Boston University MSBA

*This exercise demonstrates how digital experiments and regression modeling can quantify the real-world impact of social interventions online.*
