# Marketing A/B Test Analysis

## Business Problem

A marketing team conducted an A/B test to evaluate whether showing advertisements (treatment group) leads to higher customer conversions compared to a public service announcement (PSA) shown to the control group.

The objective of this analysis is to:
	•	Determine whether the observed difference in conversion rates is statistically significant
	•	Quantify the magnitude of conversion lift
	•	Provide a clear business recommendation on whether running ads improves conversions

## Dataset

	•	Source: Kaggle – Marketing A/B Testing Dataset
	•	Observations: 588,101 users
	•	Groups:
	•	ad (treatment): 564,577 users
	•	psa (control): 23,524 users
	•	Key Variable:
	•	converted: Binary indicator of conversion (True/False)

## Methodology

The analysis follows a standard A/B testing framework:
	1.	Exploratory Data Analysis
	•	Group size validation
	•	Conversion rate comparison
	•	Data quality checks
	2.	Hypothesis Formulation
	•	Null hypothesis (H₀): Conversion rate is the same for ad and PSA groups
	•	Alternative hypothesis (H₁): Conversion rates differ between the two groups
	3.	Statistical Testing
	•	Two-proportion Z-test
	•	95% confidence interval estimation for conversion lift
	4.	Decision Criteria
	•	Significance level α = 0.05
	•	Both statistical and practical significance considered

## Key Results

	•	Control (PSA) conversion rate: 1.79%
	•	Treatment (Ad) conversion rate: 2.55%
	•	Absolute conversion lift: 0.77 percentage points
	•	Z-statistic: 7.37
	•	p-value: < 0.000000000001
	•	95% Confidence Interval for lift: (0.60%, 0.94%)

## Interpretation: 
Users exposed to advertisements converted at a statistically significantly higher rate than those shown a PSA. The probability that this difference occurred due to random chance is effectively zero.

## Business Recommendation

	•	Running advertisements leads to a meaningful and statistically significant increase in conversions
	•	The advertising strategy should be continued or scaled, as the lift is both reliable and practically relevant given the large user base

Even a sub-1% lift is impactful at this scale and can translate into substantial incremental revenue.

## Limitations

	•	The analysis focuses solely on conversion probability and does not account for revenue, cost per ad, or customer lifetime value
	•	User-level segmentation (e.g., by time, ad frequency, or behavior) was not explored
	•	Long-term effects of repeated ad exposure were not evaluated

## Tools & Technologies

	•	Python
	•	Pandas, NumPy
	•	SciPy, Statsmodels
	•	Matplotlib, Seaborn
	•	Jupyter Notebook
