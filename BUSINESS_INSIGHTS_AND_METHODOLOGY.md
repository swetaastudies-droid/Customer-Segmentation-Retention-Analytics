# Business Insights & Methodology

## Project objective
Use customer-level data to explore customer value, purchase behavior, RFM-based segments, and recency-based retention status.

## Core questions
1. Which RFM segment has the highest historical spend?
2. Which customers have high historical value but have not purchased recently?
3. How does recency-based status vary by city or region?
4. How do Online, Offline, and App customers compare on recorded spend and repeat-purchase behavior?
5. How do loyalty tiers compare on customer count and average recorded spend?
6. Which targeted retention actions should be tested?

## Recommended interpretation format
For every insight, document:
- **Finding:** State the actual result shown in Power BI.
- **Evidence:** Add the relevant count, percentage, or spend measure.
- **Business implication:** Explain why it matters.
- **Recommendation:** Suggest an action to test.
- **Success metric:** Define how the action will be evaluated.

## Definitions and caveats
- **Historical spend:** Sum of the customer-level `Total Spend` field. Do not describe this as monthly revenue.
- **Recency days:** Number of days between the analysis date and each customer's last purchase date.
- **Retention status:** In this learning project, status labels are assigned using illustrative recency thresholds. Confirm or recalculate them consistently before analysis.
- **Retention rate proxy:** Retained customers divided by total customers under the defined recency rule. This is not cohort retention.
- **Churn risk:** Rule-based inactivity signal, not a validated predictive model.
- **Profitability:** Cannot be determined without cost data.
- **Region comparisons:** Check the number of customers in each group; small groups can produce unstable percentages.
- **Channel comparisons:** Higher spend does not necessarily mean higher profitability or marketing ROI.

## Suggested actions to test
- Champions: VIP experiences, referrals, and relevant cross-sell.
- Loyal Customers: personalised recommendations and repeat-purchase journeys.
- Potential Loyalists: onboarding, reminders, and relevant product suggestions.
- At Risk - High Value: targeted win-back and service recovery.
- Hibernating: low-cost reactivation tests.
- Needs Attention: investigate satisfaction and purchase barriers.

Treat these as hypotheses. Use campaign results and transaction-level data to validate them.
