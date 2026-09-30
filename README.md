# Cookie Cats A/B Test — Game Gate Placement & Player Retention

An end-to-end A/B testing analysis evaluating whether moving the first
progression gate from **level 30 to level 40** affected player retention
and engagement.

**Tools:** Python · Pandas · NumPy · SciPy · Statsmodels · Matplotlib · Seaborn

---

## Business Question

Should Cookie Cats move its first progression gate from **level 30 to level
40**?

### Primary Metric

**7-day player retention**

### Secondary Metrics

- 1-day player retention
- Total game rounds played

### Objective

Evaluate the experiment using descriptive analysis, statistical hypothesis
testing, effect size, and confidence intervals, then translate the findings
into a product recommendation.

## Key Findings

| Metric | Gate 30 | Gate 40 | P-Value | Significant |
|---|---:|---:|---:|:---:|
| 1-Day Retention | 44.82% | 44.23% | 0.0744 | No |
| 7-Day Retention | 19.02% | 18.20% | 0.0016 | Yes |
| Median Game Rounds | 17 | 16 | 0.0502 | No |

### Primary Finding

The gate-40 configuration produced a **0.82 percentage-point decrease in
7-day retention** compared with gate-30.

The estimated relative change was **−4.31%**, with a **95% confidence interval
of −1.33 to −0.31 percentage points**.

Because the primary 7-day retention result was statistically significant at
α = 0.05, the analysis recommends **retaining the gate-30 configuration rather
than rolling out gate-40**.
## Methodology

The analysis followed a structured A/B testing workflow:

1. **Data Validation**
   - Verified 90,189 player records
   - Checked for missing values and duplicate records
   - Confirmed one record per unique player
   - Validated experiment-group allocation

2. **Exploratory Analysis**
   - Compared 1-day and 7-day retention across experiment groups
   - Visualized retention differences between gate-30 and gate-40

3. **Statistical Testing**
   - Used two-proportion z-tests for retention metrics
   - Used α = 0.05 as the statistical significance threshold
   - Used 7-day retention as the primary metric

4. **Effect Size & Uncertainty**
   - Calculated the absolute difference in 7-day retention
   - Calculated relative change
   - Estimated a 95% confidence interval

5. **Secondary Engagement Analysis**
   - Compared median and mean game rounds
   - Used the Mann–Whitney U test because game-round counts are highly variable

6. **Business Recommendation**
   - Translated the statistical findings into a product-level recommendation
