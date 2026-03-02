# Respiratory Pathogen Surveillance Analysis (January 2026)

## Project Overview
This project provides a comprehensive Exploratory Data Analysis (EDA) of respiratory pathogen surveillance data from January 2026. The workflow transforms a "noisy" raw dataset into a refined clinical narrative covering 491 unique patient cases.

## Data Pipeline & Methodology
The project is organized into three specialized Jupyter Notebooks to maintain a clear audit trail:

### Notebook 1: Structural Cleaning

- **Focus:** Initial data integrity and format standardization.
- **Integrity Checks:** Identified and removed identical redundant records (barcode/ID level) to prepare for clinical                         analysis.

### Notebook 2: Categorical, Numeric & Deduplication Cleaning

- **Categorical Cleaning:** Standardized pathogen names and regional labels to ensure consistency in grouping.
- **Numeric Cleaning:** Addressed "Age 0" neonates and infants by converting age data from floats to integers for accurate demographic        grouping.
- **Missing Value Strategy:** Explicitly did not mitigate missing values using clinical median imputation, choosing instead to preserve       the transparency of raw surveillance gaps.
- **Deduplication & Grouping:** Performed advanced grouping of collection dates to arrive at the final count of 491 unique rows.

### Notebook 3: Exploratory Data Analysis (EDA)

- **Temporal Analysis:** Visualized the daily "heartbeat" of the outbreak using an annotated Stacked Area Plot (Epidemic Curve).
- **Bivariate Analysis:** Explored the relationship between Age Groups and Clinical Severity using boxplots.
- **Pathogen Distribution:** Mapped the regional spread of Influenza A, SARS-CoV-2, and Unknown etiologies.

## Key Findings

- **The January 25th Peak:** Identified the month's absolute peak of 24 unique cases, driven by a notable surge in "Unknown" pathogens.
- **Pathogen Dominance:** Influenza A was the primary driver of the seasonal epidemic pattern throughout the month.
- **Clinical Uniformity:** Confirmed that while all ages are vulnerable, the median clinical severity remained consistent (approx. 3.0)       across adult cohorts.

## Visualizations & Color Palette
- Green (#117733): Influenza A
- Blue (#88CCEE): SARS-CoV-2
- Red/Pink (#CC6677): Unknown Etiology
