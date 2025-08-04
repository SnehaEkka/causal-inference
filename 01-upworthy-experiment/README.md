# Upworthy Experiment Analysis

## Overview

This exercise examines real-world A/B testing by Upworthy—pioneers in using randomized experiments to optimize social media headlines for maximum engagement. The notebook walks through hands-on data exploration and statistical analysis rooted in the potential outcomes framework, a foundational concept in causal inference.

## Tools Used
- **Python 3.x**
- **Jupyter/IPython Notebook**
- **pandas** (data analysis)
- **NumPy** (numerical computation)
- **seaborn/matplotlib** (data visualization)

## Business Objective

**Key Questions:**
- How can businesses rigorously compare competing content (e.g., headlines) to maximize user engagement?
- How do we estimate and interpret causal effects in digital experiments, both at the average and individual level?

**Purpose:**  
This analysis equips practitioners with practical skills to frame, analyze, and visualize experiments, directly supporting evidence-based decision-making in content optimization, marketing, and product design. By working with real data, the exercise bridges the gap between theoretical causal methods and actionable business insights.

## Dataset Snapshot

The Upworthy dataset captures a randomized experiment on headline performance, including:
- **headline**: The headline shown to the user.
- **slug**: URL for the headline.
- **eyecatcher_id**: ID for the accompanying image.
- **clicked**: Indicator (1/0) for whether the user clicked the headline.

Each row represents a single user impression. The dataset supports granular analysis of click-through behavior by headline, as well as construction and understanding of variables used in A/B testing.

## Exercise Structure & Methods

### 1. Real-World Experiment Analysis

- **Data Exploration:** Load experimental data, confirm structure and columns, preview sample rows.
- **Variable Engineering:**  
  - Create indicator features (e.g., whether URLs mention certain keywords).
  - Generate (for demonstration) a random variable for example/statistical use.
- **Headline Analytics:**  
  - Calculate number and share of unique headlines.
  - Determine click rates by headline and rank them.
  - Visualize headline click performance using clear, publication-quality bar charts.
- **Subset & Filter:**  
  - Extract subset where users clicked to support targeted analyses.

### 2. Introduction to the Potential Outcomes Framework

- **Scenario:** Analyze individual-level effects of a hypothetical website feature ("Q&A on product pages") on user revenue.
- **Key Skills Practiced:**
  - Define and compute individual-level and average treatment effects (ITE & ATE).
  - Understand and confirm treatment effects using code and narrative.
  - Simulate randomized assignments, calculate realized outcomes, and compare to the true ATE.
  - Use Python (NumPy) to calculate empirical quantiles of the treatment effects.
  - Write reasoned, business-style interpretations alongside code for clear communication.

## Key Insights & Results

- **Engagement Optimization:** Rigorous headline testing reveals measurable differences in click performance. Quantitative analysis pinpoints the most effective headlines for boosting user engagement.
- **Causal Impact:** The potential outcomes approach clarifies the estimation (and limits) of causal effects at both the individual and group level—critical for making valid business recommendations.
- **Visualization:** Effective use of Python plotting libraries provides clear, instantly interpretable insights for stakeholders.

## How to Use / Run

1. Download the IPython notebook (`BA830-Ex-1-Upworthy-Experiment.ipynb`) and the corresponding data file (CSV).
2. Open the notebook in Jupyter Lab/Notebook or cloud environment (Colab, Codespaces).
3. Run cells sequentially to reproduce all analysis, plots, and interpretations.

**Note:** The data file is referenced in the notebook and aligned to the column/sample structure shown above.

## Requirements

- Python ≥ 3.7  
- pandas, numpy  
- seaborn/matplotlib for plotting

## Learning & Takeaways

- Developed real-world skills in experimental design, A/B testing, and causal effect interpretation.
- Learned to structure and visualize business experiments for clarity and impact.
- Practiced translating analytical findings into plain language recommendations for business stakeholders.

## Project Details

- **Completed:** January 2024  
- **Course:** Business Experimentation & Causal Methods (BA830), Boston University MSBA

*This exercise demonstrates the power of experimentation and modern causal analysis for actionable business decision-making in digital content and beyond.*
