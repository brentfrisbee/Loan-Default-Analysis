# Executive Summary:
I queried loan default data using SQL to identify borrower and loan characteristics associated with higher default risk. Based on this analysis, I identified several patterns and developed corresponding business recommendations:

* Both borrower demographics and loan attributes are associated with higher default rates

* Age group, income level, and interest rate show particularly strong relationships with default risk, in some cases exhibiting default rates nearly twice the portfolio average

* Targeted, risk-based underwriting adjustments may help reduce defaults among higher-risk segments while preserving lending capacity

# Business Problem:
Maintaining a low loan default rate is critical for the bank’s risk management, profitability, and ability to extend credit. The bank’s current default rate is approximately 11%, while the target range is 5–10%. Lenders suspect that certain borrower and loan characteristics may be contributing disproportionately to elevated default rates.

The objective of this analysis is to identify which borrower and loan attributes are most strongly associated with higher default rates and to propose data-driven actions that could help reduce overall risk.

# Results and Business Recommendations:
After querying and aggregating the data in SQL, several clear patterns emerged across borrower and loan segments:

* Interest Rate: Loans with high interest rates exhibited approximately 50% higher default rates than the portfolio average, largely independent of borrower demographics.

* Income Level: Low-income borrowers defaulted at nearly twice the average rate.

* Age Group: Age showed the strongest relationship with default risk, with borrowers under 25 experiencing an approximate 21% default rate.

These results indicate that default risk is not evenly distributed across the portfolio and that certain segments consistently exhibit higher risk profiles.

<img width="496" height="445" alt="image" src="https://github.com/user-attachments/assets/cd22b427-1488-4afc-943e-6bf98494c5ff" />

# Risk Score

<img width="418" height="187" alt="image" src="https://github.com/user-attachments/assets/f2dd3c9c-4b5f-47ee-bd9e-48d8453f42d9" />

I used SQL window functions to bucket borrowers into deciles based on credit score, debt-to-income ratio, and income. This allowed me to normalize different financial variables onto a comparable scale and identify relative risk segments across the loan portfolio. The output can be used to build a simple risk scorecard or to analyze default rates across borrower segments.


# Recommendations:

Based on these findings, I recommend the following risk-mitigation strategies:

* Implement enhanced risk controls for higher-risk segments, such as additional income verification, lower loan-to-value thresholds, or adjusted pricing structures.

* Reevaluate underwriting policies for high-interest loans, as elevated interest rates appear to be a strong indicator of default risk regardless of borrower demographics.

* Use borrower age and income as part of a broader, risk-based assessment framework rather than as exclusionary criteria, ensuring fair lending practices while improving portfolio performance.

These findings are correlational and exploratory in nature; further analysis using multivariate modeling could help quantify the independent impact of each factor and support more precise policy decisions.
