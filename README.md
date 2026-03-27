# Star Digital Advertising Effectiveness Analysis

A causal marketing analytics project that evaluates whether online display advertising increases conversions, how ad frequency affects purchase probability, which publisher sites perform best, and how ad budget should be allocated to maximize ROI.

## Overview

This project analyzes a randomized advertising experiment for Star Digital to measure the true impact of online display ads on customer purchases. Using treatment/control assignment and logistic regression models, the analysis estimates advertising lift, frequency effects, site-level effectiveness, and budget allocation tradeoffs across publisher channels.

## Business Problem

Star Digital wanted to know:

1. Does online advertising actually increase conversion rates?
2. Is there a frequency effect from repeated ad impressions?
3. Which publisher sites perform best?
4. How should advertising budget be allocated across channels?

Because the dataset comes from a randomized experiment, the project focuses on causal inference rather than simple correlation.

## Dataset

The dataset contains user-level advertising experiment data with variables including:

- `purchase`: whether the user made a purchase
- `test`: treatment vs. control group indicator
- `imp_1` to `imp_6`: ad impressions across six publisher sites

The project notes that the sample used choice-based sampling, with buyers oversampled relative to the true population purchase rate, so interpretation of probabilities required adjustment.

## Methods

The analysis was completed in **R** using:

- `dplyr` for data wrangling
- `ggplot2` for visualization
- logistic regression for conversion modeling
- t-tests for treatment/control comparison
- nonlinear modeling for diminishing returns
- ROI estimation using impression costs and predicted incremental conversions

## Key Analyses

### 1. Advertising Effectiveness
Compared conversion rates between treatment and control groups and estimated the causal effect of ad exposure using a logistic regression model.

### 2. Frequency Effect
Created a total impressions variable and modeled how repeated ad exposure changes purchase probability. A quadratic specification was used to test for diminishing returns.

### 3. Site-Level Performance
Estimated separate impression effects for Sites 1–6 to identify which publisher sites were most effective at increasing conversions.

### 4. Budget Allocation
Compared Sites 1–5 versus Site 6 using effectiveness and advertising cost assumptions to recommend an ROI-based channel allocation strategy.

## Key Findings

- Online advertising had a positive but modest effect on conversion.
- Additional impressions increased purchase likelihood, but returns diminished at high exposure levels.
- Site effectiveness varied significantly across publishers.
- Site 4 was the strongest performer on a per-impression basis.
- Site 6 produced the highest ROI due to lower cost and stronger follow-up frequency performance.
- A hybrid strategy was recommended: use Sites 1–5 for awareness and Site 6 for repeated reinforcement.

## Files

- `project.R` – R code for data preparation, modeling, and visualization
- `Social & Cust Project.pdf` – written report with business context, results, and recommendations

## Skills Demonstrated

- Marketing analytics
- Causal inference
- Logistic regression
- ROI analysis
- Experimental design
- Data visualization in R
- Business recommendation development

## Tools

- R
- dplyr
- ggplot2

