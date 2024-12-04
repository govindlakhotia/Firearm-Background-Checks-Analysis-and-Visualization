# Firearm Background Checks: Analysis and Visualization

## About the Dataset

The dataset used in this project contains records of firearm background checks conducted across various states in the United States. It includes:

    Time Period: Historical records spanning several months/years.
    Columns:
    1. month: The month when the background checks occurred (e.g., "2023-09").
    2. state: The state where the background checks were performed (e.g., "California").
    3. permit: Number of permit-related background checks.
    4. permit_recheck: Number of permit rechecks.
    5. handgun: Number of handgun background checks.
    6. long_gun: Number of long gun background checks.
    7. other: Background checks for other firearm types.
    8. multiple: Multiple firearm purchase background checks.
    9. admin: Administrative checks.
    10. prepawn_handgun: Background checks for handguns pre-pawned.
    11. prepawn_long_gun: Background checks for long guns pre-pawned.
    12. prepawn_other: Background checks for other firearms pre-pawned.
    13. redemption_handgun: Redemption checks for handguns.
    14. redemption_long_gun: Redemption checks for long guns.
    15. redemption_other: Redemption checks for other firearms.
    16. returned_handgun: Handguns returned to owners.
    17. returned_long_gun: Long guns returned to owners.
    18. returned_other: Other firearms returned to owners.
    19. rentals_handgun: Handgun rentals.
    20. rentals_long_gun: Long gun rentals.
    21. private_sale_handgun: Private sales of handguns.
    22. private_sale_long_gun: Private sales of long guns.
    23. private_sale_other: Private sales of other firearms.
    24. return_to_seller_handgun: Handguns returned to sellers.
    25. return_to_seller_long_gun: Long guns returned to sellers.
    26. return_to_seller_other: Other firearms returned to sellers.
    27. totals: Total background checks for all firearm-related transactions.

## Data Source

The dataset originates from [NICS Firearm Background Checks](https://github.com/BuzzFeedNews/nics-firearm-background-checks/tree/master/data).

## Project Objective

The primary objective of this project is to:

    1. To analyze trends in firearm background checks across states and firearm types over time.
    2. To identify key patterns and relationships in firearm purchases, rentals, and returns.
    3. To provide actionable insights for law enforcement, policymakers, and firearm businesses.
    4. To facilitate real-time monitoring and decision-making using a dynamic Grafana dashboard.
    
## Key Trends Observed

    1. State-Wise Trends:
        •States with the highest background checks consistently include [e.g., Texas, California, etc.].
        •Certain states show seasonal spikes in background checks, potentially influenced by hunting seasons or legislative changes.

    2. Firearm Types:
        •Handguns and long guns constitute the majority of background checks.
        •There is a notable increase in private sales and multiple firearm purchases over specific periods.

    3. Transaction Patterns:
        •Pre-pawn and redemption transactions show a downward trend, possibly indicating changing consumer behavior.
        •Rentals remain a minor category but indicate localized demand spikes in certain states.

## Analytical Insights

**Graph 1: Total Background Checks Over Time**

    Insight:
        Shows fluctuating trends with occasional peaks, likely tied to legislative changes or major societal events.
        Recent data indicates a steady upward trend in background checks.
    Implication:
        Indicates increasing demand for firearms, requiring resources to handle peak periods.

**Graph 2: Background Check by Firearm Type**

    Insight:
        Handguns consistently dominate, followed by long guns and "other" firearm types.
        Peaks often align with spikes in total checks, reflecting seasonal or event-driven demand.
    Implication:
        Firearm manufacturers and retailers can use this data to optimize inventory and marketing efforts.

**Graph 3: State-Wise Totals**

    Insight:
        Illinois, Kentucky, and Texas contribute the most to background checks.
        Other states like Florida and Pennsylvania also show significant activity.
    Implication:
        Policymakers in high-contributing states may need to allocate additional resources for background check processing.

**Graph 4: Permit vs Rechecks Over Time**

    Insight:
        Permits dominate over rechecks but show similar trends in peaks.
    Implication:
        States with high permit rechecks may require streamlined administrative processes to handle repeat checks.

**Graph 5: Most Active States (Pie Chart)**

    Insight:
        The top 5 states account for a significant portion of total background checks.
    Implication:
        Indicates regional concentration of firearm ownership or legislative requirements.

**Graph 6: Multiple Firearm Checks Over Time**

    Insight:
        Peaks in multiple firearm checks align with overall background check trends.
    Implication:
        May require closer scrutiny to identify patterns of bulk purchases.

**Graph 7: Returned Firearms Breakdown**

    Insight:
        Handguns dominate return transactions, followed by long guns.
    Implication:
        Insights into consumer behavior and secondary firearm markets.

**Graph 8: Rentals Over Time**

    Insight:
        Rentals show minimal activity compared to other firearm types.
    Implication:
        Indicates limited interest in firearm rentals, possibly a niche market.

**Graph 9: Private Sales by Firearm Type**

    Insight:
        Handgun private sales dominate, with occasional spikes in long guns.
    Implication:
        Highlights areas for policy focus on private sales transparency.

**Graph 10: Pre-Pawn Transactions Over Time**

    Insight:
        Pre-pawn transactions show a declining trend over time.
    Implication:
        May reflect changing consumer preferences or financial conditions.

**Graph 11: Firearm Redemption Trends**

    Insight:
        Handgun redemptions outpace long guns and others.
    Implication:
        Reflects consumer preferences in recovering pre-pawned firearms.

**Graph 12: Return to Seller Breakdown**

    Insight:
        Returns to sellers for handguns and long guns occur at similar rates.
    Implication:
        Insights into inventory management for firearm retailers.

## Dashboard Design

![Screenshot from 2024-12-01 16-39-58](https://github.com/user-attachments/assets/9a80d623-dca1-4028-bce9-ba0bf28bb223)
![Screenshot from 2024-12-01 16-40-21](https://github.com/user-attachments/assets/a2456559-2f35-488c-a952-84679a81880e)

## Video

https://github.com/user-attachments/assets/cb2311dd-f43f-4fd9-85d8-a61990c22c14


## Managerial and Policy Implications

**1. Resource Allocation:** Insights can help allocate resources (e.g., law enforcement, administrative staff) to states or months with higher transaction volumes.

**2. Policy Evaluation:** Trends in private sales and multiple firearm purchases provide feedback on the effectiveness of existing firearm legislation.

**3. Market Trends:** Understanding consumer preferences between firearm types (e.g., handguns vs. long guns) can inform manufacturers and retailers.

**4. Geographical Focus:** States with consistently high firearm background checks can be prioritized for targeted interventions or public awareness campaigns.

**5. Seasonal Planning:** Seasonal spikes in background checks highlight the need for temporary resource scaling during peak periods.

## Technical Workflow

    1. Data Processing:
        •The dataset was transformed into InfluxDB line protocol format using a Python script.
        •Data was streamed to InfluxDB using the TIG stack.

    2. Visualization:
        Grafana was used to create 12 visualizations, including:
            •Time series plots for trends over time.
            •Stacked bar charts for state-wise and category-wise breakdowns.
            •Pie charts for most active states.

    Dashboard Features:
        •Dynamic filters for states and firearm categories.
        •Alerts for significant changes in trends.
