# Safety Nets Effect on Climate-Vulnerable Women’s Health  
### Internally Migrated from Northern Bangladesh

## Overview

This repository contains the analysis workflow for a mixed-methods study on climate-displaced women living in informal settlements in Dhaka, Bangladesh.

The study examines whether social safety nets improve the health and livelihood outcomes of women who migrated from climate-affected northern districts to three Dhaka slums: Korail, Kallyanpur, and City Colony.

Using household survey data, qualitative field evidence, and regression-based analysis, the project evaluates how social protection, clinic access, displacement pathways, income, and institutional barriers shape women’s health vulnerability after migration.

## Study Context

Bangladesh is highly vulnerable to climate-related hazards such as drought, river erosion, flooding, and food insecurity. These pressures contribute to internal migration, with many displaced women relocating to urban informal settlements where they face insecure housing, limited healthcare access, sanitation constraints, and exclusion from formal support systems.

This project focuses on the gap between nominal safety-net availability and actual protection for climate-displaced women in urban slum contexts.

## Data and Methods

The study uses a convergent mixed-methods design, combining quantitative and qualitative evidence.

### Quantitative component

- Household survey of 120 households
- Individual-level information covering 342 household members
- Variables on migration history, safety-net receipt, income, employment, health, hygiene, and clinic access
- Fisher’s Exact Tests for categorical associations
- Non-parametric tests for skewed income outcomes
- Logistic regression for adjusted predictors of good self-reported health

### Qualitative component

- Focus group discussions
- In-depth interviews
- Key informant interviews
- Thematic analysis of institutional exclusion, documentation barriers, informal fees, healthcare access, and reliance on community intermediaries

## Key Findings

### 1. Safety nets support livelihood transitions

Safety-net receipt is associated with improved post-migration employment transitions. This suggests that social protection may help displaced women stabilize livelihoods after migration.

### 2. Safety nets do not independently predict health

After accounting for structural mediators, safety-net participation does not independently predict good self-reported health.

### 3. Clinic access is the strongest health predictor

Access to nearby healthcare services is the most robust predictor of good self-reported health in the adjusted model.

### 4. Displacement pathways matter

Health vulnerability varies by type of displacement, with higher disease burden observed among women displaced through drought and food-insecurity-related pathways.

### 5. Structural barriers shape vulnerability

Documentation barriers, local gatekeeping, informal fees, and limited service access prevent many women from converting formal entitlements into usable health protection.

## Repository Structure

```text
.
├── README.md
├── scripts/
│   └── 01_clean_analyze_model.R
├── outputs/
│   ├── figures/
│   │   ├── adjusted_odds_ratios_good_health.png
│   │   ├── employment_improvement_by_safety_net.png
│   │   ├── health_by_safety_net_receipt.png
│   │   └── kitchen_cleanliness_by_education.png
│   └── tables/
│       ├── h2_employment_by_safety_net.csv
│       ├── h3_income_by_duration_group.csv
│       ├── h4_kitchen_cleanliness_by_education.csv
│       ├── h5_income_by_displacement_group.csv
│       └── logistic_regression_odds_ratios.csv
