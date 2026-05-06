# Data Source and Structure

## Overview

This repository is based on primary mixed-methods fieldwork conducted for the study:

**Safety Nets Effect on Climate-Vulnerable Women’s Health: Internally Migrated from Northern Bangladesh**

The study examines whether social safety nets improve the health and livelihood outcomes of climate-displaced women living in informal settlements in Dhaka, Bangladesh. The quantitative component uses a household survey of **120 households**, while the broader study also includes qualitative interviews, focus group discussions, and key informant interviews.

The study focuses on women who migrated internally from climate-vulnerable northern districts of Bangladesh due to drought, river erosion, flooding, crop loss, food insecurity, and related livelihood stressors.

---

## Study Sites

Data were collected from three informal settlements in Dhaka:

| Study Site | Sample Size |
|---|---:|
| Korail Slum | 40 households |
| Kallyanpur Porah Slum | 40 households |
| City Colony Slum | 40 households |
| **Total** | **120 households** |

Each site contributed 40 households to the final survey sample.

---

## Sampling Design

The study used a stratified household sampling approach. Within each slum, sub-areas were identified through field mapping, and household samples were allocated proportionally across those sub-areas.

### Korail Slum

| Sub-area | Estimated Households | Sample Size |
|---|---:|---:|
| Beltola | 2,274 | 7 |
| Bou Bazar | 5,059 | 16 |
| Jamai Bazar | 5,370 | 17 |
| **Total** | **12,703** | **40** |

### Kallyanpur Porah Slum

| Sub-area | Estimated Households | Sample Size |
|---|---:|---:|
| Dakshin Paikpara | 950 | 10 |
| Madhya Paikpara | 1,000 | 11 |
| Uttar Paikpara | 800 | 9 |
| Kallyanpur Mahalla | 950 | 10 |
| **Total** | **3,700** | **40** |

### City Colony Slum

| Sub-area | Estimated Households | Sample Size |
|---|---:|---:|
| Near Buddhijibi Monument | 600 | 15 |
| Near Graveyard | 500 | 12 |
| Inner Alley | 500 | 13 |
| **Total** | **1,600** | **40** |

The quantitative sample was selected to represent climate-displaced households across the three study locations. Qualitative participants were recruited through community contacts, NGOs, and snowball sampling to capture lived experiences of migration, health insecurity, and institutional exclusion.

---

## Data Collection

The study used a convergent mixed-methods design.

### Quantitative Component

The household survey collected information on:

- migration origin and reason for displacement
- years since migration to Dhaka
- employment before and after migration
- income before and after migration
- access to social safety nets
- health-related aid receipt
- clinic access
- self-reported illness and health status
- education level
- hygiene practices
- household vulnerability indicators

### Qualitative Component

The broader study also included:

- 30 semi-structured in-depth interviews
- 6 focus group discussions
- 5 key informant interviews

These qualitative sources were used to contextualize the survey findings and explain barriers related to documentation, informal fees, local gatekeeping, healthcare access, and reliance on community intermediaries.

---

## Main Data Components

The analysis draws on several linked data components from the household survey and appendix tables.

### 1. Sampling and Study Design

Includes:

- slum-level household estimates
- sub-area sampling allocation
- proportional sample distribution
- sampling technique

### 2. Migration and Income Data

Includes:

- household ID
- homeplace before migration
- migration companion
- vehicle or mode of migration
- income before migration
- income after migration
- employment before migration
- employment after migration

### 3. Displacement Drivers

Includes reported reasons for migration, such as:

- drought
- crop damage
- river erosion
- flooding
- starvation due to natural calamities
- loss of work due to climate vulnerability
- land loss
- climate disaster-related occupational change

### 4. Health and Aid Variables

Includes:

- health-related aid received
- aid receipt status
- type of aid received
- source of aid, including government, NGO, and UN agency support
- clinic or community healthcare access
- free medicine or vaccination access
- government treatment access

### 5. Education and Hygiene Variables

Includes:

- education level
- handwashing after toilet use
- handwashing before eating
- kitchen cleanliness
- household sanitation-related indicators

### 6. Analytical Outputs

The repository documents analysis related to:

- descriptive summaries
- hypothesis-based bivariate tests
- Fisher’s exact tests
- non-parametric income comparisons
- logistic regression modeling
- odds ratios and confidence intervals
- figure generation

---

## Key Variables Used in the R Analysis

| Variable | Description |
|---|---|
| `household_id` | Unique household identifier |
| `safety_net_binary` | Whether the respondent received safety-net or aid support |
| `aid_received_on_health` | Type or status of health-related aid received |
| `self_health` | Derived self-reported health category |
| `good_health` | Binary health outcome used in logistic regression |
| `clinic_access` | Whether the respondent had access to a nearby clinic or health service |
| `income_before` | Household income before migration |
| `income_after` | Household income after migration |
| `income_after_k` | Post-migration income scaled per 1,000 BDT |
| `employment_before` | Employment status before migration |
| `employment_after` | Employment status after migration |
| `employment_improved` | Whether employment status improved after migration |
| `years_staying_in_dhaka` | Duration of residence in Dhaka |
| `duration_group` | Categorized migration duration |
| `major_reason_of_displacement` | Original reported reason for climate-related migration |
| `displacement_group` | Grouped displacement pathway |
| `education_level` | Reported education level |
| `edu_group` | Recoded education category |
| `kitchen_clean` | Binary kitchen cleanliness indicator |
| `wash_before_eating` | Binary handwashing indicator before eating |
| `types_of_health_problems` | Reported illness or health condition combinations |

---

## Variable Construction Notes

Several variables used in the R analysis were recoded or derived from raw survey responses.

### Health Outcome

Self-reported health was derived from reported illness frequency and grouped into interpretable categories. The logistic regression model uses a binary outcome for good self-reported health.

### Safety-Net Receipt

Safety-net participation was coded as a binary indicator based on whether respondents reported receiving any form of government, NGO, or institutional assistance.

### Employment Improvement

Employment improvement was constructed by comparing employment status before and after migration.

### Income

Income before and after migration was cleaned and converted into numeric BDT values. Post-migration income was also scaled per 1,000 BDT for regression interpretation.

### Displacement Group

Detailed displacement reasons were grouped into broader categories to support hypothesis testing and visualization.

### Education and Hygiene

Education levels were recoded into broader education groups. Hygiene indicators were converted into binary variables for handwashing and kitchen cleanliness.

---

## Data Privacy and Availability

The raw household-level dataset is **not publicly shared** because it contains sensitive respondent-level information from climate-displaced women living in informal settlements.

This repository includes:

- R scripts documenting the analysis workflow
- selected figures
- selected model outputs
- variable-construction logic
- summary-level documentation

This repository does **not** include personally identifiable or sensitive raw respondent-level records.

---

## Reproducibility Note

The analysis code is provided to document the quantitative workflow, including data cleaning, variable construction, hypothesis testing, regression modeling, odds-ratio estimation, and figure generation.

Because the raw dataset is restricted for ethical and confidentiality reasons, external users may not be able to fully reproduce the results without access to the protected survey data. However, the repository is structured to make the analysis logic transparent and reviewable.

---

## Suggested Repository Structure

```text
.
├── README.md
├── DATA_SOURCE.md
├── Scripts/
│   ├── 01_clean_analyze_model.R
│   └── readme.md
├── figures/
│   ├── HYpo1ODDSratio.jpeg
│   ├── Hypo-1: self reported health.jpeg
│   ├── Hypo 2: Employment graph.jpeg
│   ├── Hypo 3(b): Income After Migration.jpeg
│   ├── Hypo 4(a): Kitchen Cleanliness and Education.jpeg
│   ├── Hypo 4(b): Handwashing and education.jpeg
│   ├── Hypo 5: Health vs displacement.jpeg
│   └── Hypo5(b): Income Distribution vs displacement.jpeg
└── outputs/
    └── tables/
