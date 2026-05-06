# Data Source and Structure

## Data Source

This project is based on primary household survey data collected for the study:

**Safety Nets Effect on Climate-Vulnerable Women’s Health: Internally Migrated from Northern Bangladesh**

The survey covered **120 households** across three informal settlements in Dhaka, Bangladesh:

- Korail Slum
- Kallyanpur Porah Slum
- City Colony Slum

The study focused on climate-displaced women who migrated from northern Bangladesh due to climate-related stressors such as drought, river erosion, flooding, crop loss, and food insecurity.

## Sampling Design

A stratified household sampling design was used across the three study sites. Each slum contributed 40 households to the final sample.

| Study Site | Sample Size | Sampling Approach |
|---|---:|---|
| Korail Slum | 40 households | Proportional sampling across sub-areas |
| Kallyanpur Porah Slum | 40 households | Proportional sampling across sub-areas |
| City Colony Slum | 40 households | Proportional sampling across sub-areas |
| **Total** | **120 households** | Stratified household survey |

The sampling design was based on field mapping of household population estimates in each slum sub-area.

## Main Data Components

The analysis draws on several linked components from the household survey and appendix tables.

### 1. Sampling and Study Design

Contains information on:

- Slum sub-areas
- Estimated household counts
- Proportional sample allocation
- Sampling technique

### 2. Migration and Income Data

Contains household-level information on:

- Homeplace before migration
- Migration companions
- Vehicle or pathway of migration
- Income before migration
- Income after migration
- Employment before migration
- Employment after migration

### 3. Health and Aid Variables

Contains information on:

- Health-related aid received
- Aid receipt status
- Type of aid received
- Aid source, including government, NGO, and UN agency support
- Education level
- Handwashing practices
- Kitchen cleanliness

### 4. Health Conditions and Aid Receipt

Contains household-level illness and aid information, including:

- Types of reported health problems
- Whether health-related aid was received
- Type of assistance received, such as free medicine, vaccination, or government treatment

### 5. Education and Hygiene Variables

Contains information on:

- Educational attainment
- Literacy level
- Handwashing after toilet use
- Handwashing before eating
- Kitchen cleanliness

### 6. Regression and Hypothesis Testing Outputs

Contains summarized analytical outputs, including:

- Logistic regression results for good self-reported health
- Odds ratios and confidence intervals
- Summary of hypothesis testing results

## Key Variables Used in the R Analysis

| Variable | Description |
|---|---|
| `household_id` | Unique household identifier |
| `safety_net_binary` | Whether the respondent received safety-net support |
| `aid_received_on_health` | Type or status of health-related aid received |
| `self_health` | Derived self-reported health category |
| `good_health` | Binary health outcome used in logistic regression |
| `clinic_access` | Whether the respondent had access to a nearby clinic |
| `income_before` | Household income before migration |
| `income_after` | Household income after migration |
| `income_after_k` | Post-migration income scaled per 1,000 BDT |
| `employment_before` | Employment status before migration |
| `employment_after` | Employment status after migration |
| `employment_improved` | Whether employment status improved after migration |
| `years_staying_in_dhaka` | Duration of residence in Dhaka |
| `duration_group` | Categorized migration duration |
| `major_reason_of_displacement` | Original reason for climate-related migration |
| `displacement_group` | Grouped displacement pathway |
| `education_level` | Reported education level |
| `edu_group` | Recoded education category |
| `kitchen_clean` | Binary kitchen cleanliness indicator |
| `wash_before_eating` | Binary handwashing indicator before eating |
| `types_of_health_problems` | Reported illness or health condition combinations |

## Data Privacy and Availability

The raw household-level dataset is **not publicly shared** because it contains sensitive respondent-level information from climate-displaced women living in informal settlements.

This repository includes:

- R scripts documenting the analysis workflow
- Selected summary tables
- Selected figures
- Variable construction logic
- Model outputs

The repository does **not** include personally identifiable or sensitive raw respondent-level records.

## Reproducibility Note

The analysis code is provided to document the data-cleaning, variable construction, hypothesis testing, regression modeling, and visualization workflow.

Because the raw dataset is restricted for ethical and privacy reasons, external users may not be able to fully reproduce the analysis without access to the protected survey data.

## Suggested Repository Structure

```text
.
├── README.md
├── DATA_SOURCE.md
├── scripts/
│   └── 01_clean_analyze_model.R
├── outputs/
│   ├── figures/
│   └── tables/
