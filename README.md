# Auto Insurance Claim Management Study

This project aims to analyze the claims performance of an auto insurance company by examining key metrics such as claim frequency, severity, payout accuracy,     processing time, and fraud detection effectiveness. By leveraging historical claims data, the project will identify trends, outliers, and inefficiencies. The objective is to gain actionable insights that improve operational efficiency, enhance the accuracy of reimbursements, and support strategic decision-making. Ultimately, the analysis will guide the company toward more data-driven claims management practices, optimizing both customer experience and financial performance.


## Key Findings: 

    - Loss ratio volatility is severity-driven, not frequency-driven. Claim counts are stable to declining, while average claim severity rises materially mid-year.
    
    - A small proportion of severe claims contributes disproportionately to incurred losses, settlement duration, and reserve uncertainty.

    - Loss emergence follows a predictable lag: claim intake peaks before severity, closures, and loss ratio deterioration.

    - Current pricing, reserving, and estimation frameworks underperform in the tail, increasing earnings and capital volatility.

    - Operational performance is working well. The primary risk is inflation-driven severity exceeding model and pricing assumptions.

    - Without intervention, declining frequency may mask structural profitability deterioration.


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
