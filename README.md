# US-Census-API-Data-Pull-Using-Python

📊 Regional Workforce and Economic Data Pull (Indiana Region 5)

🧭 Executive Summary

This data project was developed to support a regional workforce planning effort aimed at understanding how Central Indiana’s economy and labor market have evolved since 2019.
Using U.S. Census American Community Survey (ACS) data, the analysis examines trends in employment, industry composition, income, and poverty across Marion County, its neighboring counties, and the state of Indiana.

By consolidating these indicators into a single, reproducible dataset, this work enables planners, policymakers, and community partners to:

Quantify regional disparities in labor force participation and economic well-being.

Identify industries driving growth and those showing signs of decline or underemployment.

Ground strategic discussions in objective, longitudinal data from a reliable public source.

This dataset now serves as a foundational input to inform the region’s next strategic workforce plan, ensuring that decisions are guided by both data evidence and community insight.

🧩 Overview

This repository automates the retrieval, cleaning, and export of U.S. Census American Community Survey (ACS) data to support regional labor market and economic analysis for strategic planning purposes.

The dataset provides a consistent five-year snapshot (2019–2023) of economic, employment, and demographic trends for Marion County, Indiana, all contiguous counties, and the state of Indiana.
It enables evidence-based planning, policy alignment, and stakeholder engagement around workforce participation, industry shifts, and socioeconomic well-being.

🎯 Business Context

A regional workforce development organization commissioned this analysis as part of a multi-year strategic planning process to:

Understand post-pandemic employment patterns and structural economic changes.

Identify barriers to workforce participation and areas of underemployment.

Quantify industry composition and labor market concentration across the region.

Ground stakeholder discussions in objective, publicly available data.

The resulting dataset serves as a baseline reference for broader strategic planning efforts that also integrate qualitative stakeholder interviews, employer surveys, and policy scans.

❓ Research Questions

The following research questions guided the data extraction and analysis:

1. Labor Force Dynamics

What proportion of adults participate in the labor force?

What is the unemployment rate, and how has it changed over time?

What portion of workers are underemployed (e.g., part-time for economic reasons)?

2. Economic Well-Being

What percentage of residents live below the poverty line, and how does that vary by geography?

How have median household incomes shifted in the past five years?

What is the distribution of income and employment opportunities across counties?

3. Industry and Occupational Composition

What are the dominant industries by employment share across counties?

Which sectors have grown or declined since 2019?

How does the region’s industrial mix compare to the state as a whole?

4. Demographic and Social Characteristics

What is the age, racial, and linguistic composition of the region’s population?

What proportion of residents report a disability or veteran status?

How might these demographic indicators intersect with labor market participation?

🧰 Technical Approach
1. Data Sources

All data were retrieved directly from the U.S. Census Bureau’s API using the American Community Survey (ACS) 5-Year Estimates and County Business Patterns (CBP) datasets.
Key ACS tables included:

ACS Table	Description
S2301	Employment Status (Labor force, unemployment, underemployment)
S1701	Poverty Status in the Past 12 Months
B01003	Total Population
B19013	Median Household Income
S1810	Disability Status
S2405	Industry by Occupation for the Civilian Employed Population
2. Geographies

Marion County, IN

Contiguous counties: Boone, Hamilton, Hancock, Hendricks, Johnson, Madison, Morgan, and Shelby

Indiana statewide totals

3. Metrics Produced

Each dataset includes:

Total population and population 18+

Labor force participation rate, unemployment rate, and underemployment rate

Poverty rate (% below poverty level)

Median household income

Industry-level employment counts and shares

Demographic indicators (race, language, disability, veteran status)

4. Technical Details

API key authenticated to U.S. Census (https://api.census.gov/data)

Data collected for 2019–2023 (latest 5-year ACS vintages)

Results stored as .xlsx file with the following sheets:

ACS_Wide (raw variable codes)

ACS_Wide_Renamed (human-readable names)

ACS_Industry_Wide (industry-level data)

ACS_Industry_Wide_Renamed (industry names)

All code implemented in Python (pandas, requests, openpyxl)
