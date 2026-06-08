# Auto Insurance Claim Management Study

This project aims to analyze the claims performance of an auto insurance company by examining key metrics such as claim frequency, severity, payout accuracy,     processing time, and fraud detection effectiveness. By leveraging historical claims data, the project will identify trends, outliers, and inefficiencies. The objective is to gain actionable insights that improve operational efficiency, enhance the accuracy of reimbursements, and support strategic decision-making. Ultimately, the analysis will guide the company toward more data-driven claims management practices, optimizing both customer experience and financial performance.

For the full report, visit: https://drive.google.com/file/d/1XJiJQXSe0SpAAf0UnrhNYky75rDWVkBS/view?usp=sharing

# Executive Question
Why is profitability deteriorating despite stable claim volumes?

## Hypothesis 1: Profitability is declining because we are receiving more claims.
- Tests: Monthly claim frequency trend, Total claim count trend, Seasonal volume analysis

- Findings: Rejected
    - Claim frequency is declining.
    - Total claim counts are relatively stable
    - Loss ratio spikes do not coincide with volume spikes

- Insight: The portfolio is not becoming less profitable because more customers are filing claims

## Hypothesis 2: Profitability is declining because claim costs are increasing
- Tests: Average reimbursement trend, Severity trend analysis, Loss ratio vs severity correlation

- Findings: Supported
    - Average claim severity rises steadily throughout the year
    - Severity peaks align with loss ratio peaks
    - Loss ratio volatility closely follows claim severity

- Insight: Higher claim costs—not claim volume—are the primary driver of profitability deterioration

## Hypothesis 3: A small number of severe claims are driving most losses
- Tests: Severity distribution analysis, Tail-loss concentration analysis, Settlement duration by severity

- Findings: Supported
    - Severe claims represent a small percentage of claims
    - Severe claims account for a disproportionate share of incurred losses
    - Severe claims remain open longer and create reserve uncertainty

- Insight: This is primarily a tail-risk problem, not an average-claim problem

## Hypothesis 4: Operational inefficiency is causing poor financial results
- Tests: Processing time analysis, Closure rate analysis, Workflow performance analysis

- Findings: Rejected
    - Operational performance remains generally stable
    - Claims teams continue to process claims effectively
    - Loss ratio deterioration occurs even when operational metrics remain healthy

 - Insight: Claims operations are not the main source of profitability pressure

## Hypothesis 5: Loss ratio deterioration can be predicted before it occurs
- Tests: Lag analysis between claim intake, claim closure, severity emergence, and loss ratio changes

- Findings: Supported
    - Claim submissions peak first
    - Severity increases later
    - Loss ratio deterioration follows afterward.

- Insight: The business has an early-warning window but is not currently using it

## Hypothesis 6: Closure capacity constraints contribute to worsening results
- Tests: Submission vs closure trends, Backlog growth analysis, Settlement duration analysis

- Findings: Partially Supported
    - During July–September, closures lag submissions.
    - Backlogs build before severity peaks.
    - Delayed settlements contribute to reserve uncertainty.

- Insight: Capacity constraints amplify severity-related problems rather than create them.

## Hypothesis 7: Current reserving and pricing models accurately capture risk.
- Tests: Estimate vs actual compensation analysis, Loss development review, Severity stress testing

- Findings: Rejected
    - Estimation accuracy deteriorates sharply for severe claims.
    - Large losses create significant forecasting error.
    - Current assumptions underestimate tail risk.
    
- Insight: The models work for routine claims but break down for large losses.

## Hypothesis 8: Estimation errors are random.
- Tests: Estimation error distribution, Error patterns by agency, assignee, claim type
- Findings: Rejected
    - Errors cluster around specific handlers and claim categories
    - Error rates increase systematically with severity

- Insight: This is a process and capability issue, not random statistical noise

## Hypothesis 9: Certain vehicles and coverages are disproportionately driving losses.
- Tests: Loss ratio by vehicle type, Severity by coverage type, Portfolio mix analysis
  
- Findings: Supported
    - Private four-wheelers drive a large share of loss exposure
    - Collision and total-loss coverages generate most severity

- Insight: Risk is concentrated in specific portfolio segments

## Hypothesis 10: Early-policy claims suggest anti-selection or opportunistic behavior
- Tests: Claim timing relative to policy inception, Claim frequency by policy age

- Findings: Supported
    - Claims spike immediately after policy inception.
    - Frequency declines throughout the policy term.

- Insight: The portfolio may be exposed to anti-selection risk and requires stronger controls during early policy periods.

## Final Conclusion:

Profitability deterioration is driven by increasing claim severity and concentration of large losses, not by claim volume growth or operational failure. Existing pricing, reserving, and estimation frameworks underestimate severe-loss risk, while predictable leading indicators are not being used proactively. The business should focus on severity management, tail-risk controls, pricing adequacy, and early-warning monitoring rather than claim-volume reduction initiatives.

## Recommendations:

- Recalibrate financial assumptions for severity inflation
  - Update pricing, reserving, and reinsurance assumptions to reflect severity growth, not just frequency trends.
  - Stress-test profitability under +5%, +10%, +15% severity scenarios.

- Introduce severity-based claim controls
  - Implement early large-loss flags at FNOL with escalation thresholds.

- Apply distinct reserving logic for top 5–10% of claims.
  - Route severe claims to specialized handlers earlier.
  - Apply targeted pricing, deductibles, and underwriting controls to private four-wheelers, collision and total loss coverage

- Strengthen operational resilience mid-year
  - Add surge capacity (staffing or vendors) during July–September.
  - Prevent backlog accumulation that amplifies severity and reserve uncertainty.

- Institutionalize leading risk indicators. Track monthly indicators that move before loss ratio deterioration:
  - Severity mix (% Severe + High)
  - % estimation error
  - Backlog size
  - Settlement duration for severe claims
