# Firearm Background Checks: Analysis and Visualization

## About the Dataset

The dataset used in this project contains records of firearm background checks conducted across various states in the United States. It includes:

    Time Period: Historical records spanning several months/years.
    Columns:
        month: The date when the checks were conducted.
        state: The state where the checks occurred.
        totals: Total number of background checks.
        Various firearm-related metrics such as permit, handgun, long_gun, multiple, rentals, and redemption figures.
        Breakdown of specific transactions like prepawn_handgun, private_sale_handgun, and return_to_seller_long_gun.

## Data Source

The dataset originates from [NICS Firearm Background Checks](https://github.com/BuzzFeedNews/nics-firearm-background-checks/tree/master/data).

## Project Objective

The primary objective of this project is to:

    1. Streamline the dataset into a time-series format for real-time visualization using InfluxDB and Grafana.
    2. Analyze trends and insights into firearm-related transactions across states and time periods.
    3. Provide actionable insights for managerial decision-making, policy evaluation, and understanding the distribution of background checks.

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

**1. Total Background Checks Over Time:** A steady upward trend is observed in total background checks, indicating increasing firearm purchases or stricter checks.

**2. Most Active States:** Certain states consistently rank highest in firearm checks, likely reflecting larger populations or higher firearm ownership rates.

**3. Firearm Type Analysis:** Long guns and handguns dominate background checks, with occasional surges in other firearm types indicating shifting preferences or market trends.

**4. Impact of Events:** Background checks surged during [e.g., certain policy announcements, public safety concerns, or major events].

![Dashboard P1](https://github.com/user-attachments/assets/c0cb6a8d-34ba-4442-91be-8ac165b2065c)
![Dashboard P2](https://github.com/user-attachments/assets/6d741a54-4d2e-4dd8-9217-72951c35ec75)


## Managerial and Policy Implications

**1. Resource Allocation:** Insights can help allocate resources (e.g., law enforcement, administrative staff) to states or months with higher transaction volumes.

**2. Policy Evaluation:** Trends in private sales and multiple firearm purchases provide feedback on the effectiveness of existing firearm legislation.

**3. Market Trends:** Understanding consumer preferences between firearm types (e.g., handguns vs. long guns) can inform manufacturers and retailers.

**4. Geographical Focus:** States with consistently high firearm background checks can be prioritized for targeted interventions or public awareness campaigns.

**5. Seasonal Planning:** Seasonal spikes in background checks highlight the need for temporary resource scaling during peak periods.

## Technical Workflow**

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
