# Analytical Report: Life Insurance Death Claims Performance Analysis

## 1. Dataset Overview and Data Profile

This technical report details a comprehensive Exploratory Data Analysis (EDA) of the "li_death_claims.csv" dataset. This data provides critical insights into the performance metrics of death claims across the life insurance industry, facilitating a multi-year comparative study of operational efficiency, settlement success, and claim volumes.

### Initial Data Composition

The table below outlines the structural integrity and dimensions of the dataset upon ingestion.

| Metric                  | Detail                     |
|-------------------------|----------------------------|
| Total Number of Entries | 151                        |
| Total Number of Columns | 25                         |
| Data Types Present      | float64 (22 columns), object (3 columns) |

The dataset captures performance across 46 unique life insurers over 5 distinct reporting periods (2017-18 to 2021-22). Profiling the raw data identifies "Aegon" as the most frequent entity (5 occurrences) and the 2020-21 cycle as the most represented period (45 entries).

## 2. Data Cleaning and Pre-processing Methodology

To ensure statistical rigor and mathematical stability for downstream analysis, a systematic cleaning protocol was executed:

- **Missing Value Handling**:
    - Numeric Columns: All missing values in numerical fields were imputed using the median. This approach preserves the central tendency of the data while mitigating the influence of the extreme outliers prevalent in this industry.
    - Categorical Integrity: Records with missing 'life_insurer' (1 instance) or 'year' (2 instances) values were dropped to maintain a verified link between performance and entity.
- **Data Type Correction**: The 'year' variable was converted to a categorical format, allowing for proper chronological ordering in trend visualizations.
- **Noise Reduction and Stability**: To resolve inconsistencies from negative near-zero floating point errors, all float64 columns were clipped to a lower bound of 0.0. This step is essential for mathematical stability during the derivation of settlement and efficiency ratios.

## 3. Univariate Analysis and Distribution Insights

Examination of the frequency distributions for claim metrics reveals a significant structural trend in the marketplace:

- **Volume Concentration**: Histograms for 'claims_pending', 'claims_intimated', 'total_claims', and 'claims_paid' show a high concentration of frequency at the lower end of the scale. This confirms an industry landscape dominated by small-scale insurers or smaller claim batches, contrasted by a select few "heavyweight" outliers.
- **Industry Standards**: The distributions for claims_paid_ratio_no and claims_paid_ratio_amt are heavily skewed toward 1.0 (100%). This indicates that the vast majority of the industry maintains exceptionally high settlement rates, with 100% payout being the operational benchmark.

## 4. Outlier Detection and Data Skewness

Visual analysis via boxplots confirms that outliers are not anomalous errors but represent the high-capacity leaders of the insurance market. The raw metrics exhibit extreme positive skewness, necessitating careful statistical treatment.

### Skewness Analysis of Key Metrics

The following table provides the precise skewness values for core operational metrics.

| Metric                  | Skewness Value | Status         |
|-------------------------|----------------|----------------|
| claims_unclaimed_no     | 5.46           | Highly Skewed  |
| claims_pending_end_no   | 5.22           | Highly Skewed  |
| claims_rejected_no      | 5.15           | Highly Skewed  |
| claims_pending_start_no | 4.80           | Highly Skewed  |
| claims_paid_amt         | 4.21           | Highly Skewed  |
| total_claims_amt        | 4.16           | Highly Skewed  |
| total_claims_no         | 3.70           | Highly Skewed  |
| claims_intimated_no     | 3.70           | Highly Skewed  |

**Feature Engineering**: To address the high skewness of 'claims_intimated_no' (3.70), a log transformation (np.log1p) was applied to create a new feature: claims_intimated_no_log. This engineering step normalizes the distribution for comparative modeling while preserving the integrity of the original raw data for executive reporting.

## 5. Correlation Analysis

The Correlation Heatmap reveals critical linear relationships that define the operational flow of claims:

- **Volume Drivers**: A near-perfect positive correlation exists between total_claims_no, claims_intimated_no, and claims_paid_no. This confirms that high-volume intake is successfully met with proportional output across most insurers.
- **The Inverse Settlement Relationship**: Critically, the analysis identifies a significant negative correlation between the claims_paid_ratio_no and the claims_repudiated_rejected_ratio_no. This highlights a direct trade-off: as rejection ratios increase, the overall settlement success rate declines significantly, rather than just being a byproduct of higher volumes.
- **Ratio Independence**: Settlement ratios show a negligible correlation with raw claim counts, suggesting that an insurer’s efficiency is independent of their size or total volume handled.

## 6. Business Performance and Year-wise Trends

Temporal analysis identifies a massive shift in the insurance environment during the recent five-year window:

- **The COVID-19 Impact**: Line plots demonstrate a stable trajectory for claims paid from 2017 through 2020. However, the 2020-21 cycle saw a massive spike in claim volumes. This is directly attributable to the heightened mortality rates associated with the COVID-19 pandemic. While volumes began to normalize in 2021-22, they remain significantly higher than pre-pandemic levels.
- **Scale vs. Rejection**: Scatter plot analysis shows that while higher "Claims Paid" volumes generally correlate with higher absolute "Claims Rejected" counts, the relationship is largely linear, suggesting that rejection is a function of the increased volume processed during peak periods.

## 7. Insurer Efficiency Modelling

To evaluate performance beyond raw volume, a composite Efficiency Score was developed. This metric provides a balanced KPI by accounting for successes (payouts) while penalizing delays (pending) and failures (rejections).

**Efficiency Score Formula**: Efficiency = (claims_paid_ratio_no) - (claims_pending_ratio_no) - (claims_repudiated_rejected_ratio_no)

Our analysis shows that the industry-wide Efficiency Score has a highly negative skewness of -5.03. This indicates that while the vast majority of insurers are highly efficient (clustering near the top of the score), there is a small group of significant underperformers whose backlogs and high rejection rates drag the industry average down.

### Top 10 Insurers by Efficiency Score

Utilizing this model, we have identified the top performers who balance high volume with maximum settlement efficiency. Major industry players like LIC, Aegon, and SBI Life consistently appear as benchmarks in these efficiency and volume rankings.

## 8. Strategic Recommendations and Data Conclusions

The final refined dataset has been archived as 'cleaned_li_death_claims.csv' for further predictive analysis.

### Key Takeaways for Stakeholders

1. **Pandemic Resilience**: The industry successfully scaled operations to meet the unprecedented 2020-21 volume spike driven by COVID-19 without a systemic collapse in settlement ratios.
2. **Unclaimed Settlements Risk**: claims_unclaimed_no exhibits the highest skewness in the dataset (5.46). A specific subset of insurers is struggling with a disproportionately high number of unclaimed settlements; we recommend a targeted audit of these laggards to reduce liability.
3. **Adoption of Efficiency KPI**: Stakeholders should transition from monitoring raw payout volumes to utilizing the Efficiency Score as a primary KPI. This metric is the most effective way to identify insurers who provide high-quality service while maintaining mathematical hygiene in their claims pipeline.