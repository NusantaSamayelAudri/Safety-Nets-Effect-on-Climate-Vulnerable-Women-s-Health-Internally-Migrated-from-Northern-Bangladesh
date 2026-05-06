# Tables and Model Outputs

This folder contains selected tabular outputs from the R analysis workflow. The tables summarize descriptive patterns, hypothesis-based tests, and regression outputs used in the study.

The full analysis is based on a mixed-methods study of climate-displaced women living in three informal settlements in Dhaka: Korail, Kallyanpur, and City Colony. The quantitative component uses a household survey of 120 households, while the broader study also includes interviews, FGDs, and KIIs.

---

## Table Index

| File | Description |
|---|---|
| `logistic_regression_odds_ratios.csv` | Adjusted odds ratios, confidence intervals, and p-values from the logistic regression model predicting good self-reported health |
| `h2_employment_by_safety_net.csv` | Summary of employment improvement by safety-net receipt |
| `h3_income_by_duration_group.csv` | Post-migration income summary by duration of stay in Dhaka |
| `h4_kitchen_cleanliness_by_education.csv` | Kitchen cleanliness distribution by education group |
| `h4_handwashing_by_education.csv` | Handwashing-before-eating distribution by education group |
| `h5_income_by_displacement_group.csv` | Post-migration income summary by displacement pathway |
| `h6_income_by_safety_net.csv` | Income comparison by safety-net receipt |

---

## Main Analytical Table

The main regression output estimates predictors of good self-reported health among climate-displaced women.

Key predictors include:

- safety-net receipt
- clinic access
- income after migration
- displacement group

The model is interpreted as an adjusted association, not a causal estimate, because the survey is cross-sectional.

---
## Summary of Hypothesis-Based Results

The table below summarizes the main hypothesis-based quantitative results, excluding H1 because the primary health model is reported separately in the logistic regression output.

| Hypothesis | Relationship Tested | Test Used | Main Result | Interpretation |
|---|---|---|---|---|
| H2 | Safety-net receipt → Employment improvement | Logistic / Chi-square | OR = 2.54, p = 0.0298 | Supported. Safety-net receipt is associated with improved post-migration employment transitions. |
| H3 | Migration duration → Post-migration income | Spearman / ANOVA | ρ = -0.035, p = 0.703; ANOVA p = 0.099 | Not supported. Longer residence in Dhaka does not clearly predict higher post-migration income. |
| H4 | Education → Hygiene practices | Fisher’s Exact Test | p < 0.00001 | Supported. Education is strongly associated with hygiene-related practices. |
| H5 | Displacement type → Disease frequency | ANOVA | p = 0.0293 | Supported. Disease burden varies significantly across displacement pathways. |
| H6 | Safety-net receipt → Income recovery | Wilcoxon test | p = 0.187 | Not supported. Safety-net receipt is not significantly associated with income recovery. |
## Hypothesis-Based Outputs

The exported tables correspond to the project’s main hypothesis-based analysis:

| Hypothesis | Output Focus |
|---|---|
| H1 | Safety-net receipt, clinic access, and good self-reported health |
| H2 | Safety-net receipt and employment improvement |
| H3 | Migration duration and post-migration income |
| H4 | Education and hygiene practices |
| H5 | Displacement type, health vulnerability, and income |
| H6 | Safety-net receipt, income, and health outcomes |

---

## Interpretation Notes

- Fisher’s Exact Tests were used for categorical associations where expected cell counts were small.
- Non-parametric tests were used for skewed income outcomes.
- Logistic regression was used to estimate adjusted predictors of good self-reported health.
- Odds ratios are interpreted with confidence intervals and p-values.
- Findings should be interpreted as associational because of the cross-sectional design.

---

## Data Privacy Note

The raw household-level dataset is not publicly shared because it contains sensitive respondent-level information from climate-displaced women living in informal settlements.

This folder contains only summary-level outputs and model tables generated from the analysis workflow.
