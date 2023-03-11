# Data Audit and Base Searches

<h2>Generating KPI Values</h2>

- Once we have a basic plan for the services and their KPIs, we can work on the detailed design needed to generate the correct numeric value for each KPI.

<h2>Getting ITSI Data In</h2>

- IT Service Intelligence can consume any data in Splunk
- Data required is based on the types of services and KPIs to be monitored.
- Ideally you should have at least 7 days worth of data to work with when you begin configuring esp for Adaptive Thresholds.

# KPI Search Design Criteria
- Each KPI measures one value from the available data
- To design a KPI Search you need 
    - Search expression
    - Specific field has the value of KPI.
    - time span & frequency
    - want to split KPI results values by entities.

# KPI Data sources
1. Event Searches
2. Metric Searches

# Mapping KPIs to events and fields
- use <code>fieldsummery</code> command to help understand the structure of the data.
- For each KPI what type of events contain needed data, relevent field & what calculation to use

# KPI Design Approch
1. Run searches in Splunk to identify the content of the target sourcetypes, identify the fields and calculation fields.
2. Use built-in modules to rapidly generate KPIs

# Best Practices
- Search must return single value
- Use single source if possible.
- Use simple seach, avoid wild cards, data model/transforming commands like stats.
- Use the least frequent schedule possible.
- Use shortest time span possible (Smaller results search = less resource use).

# <code>fieldsummary</code> command
- Examine this source type with fieldsummary.
- The <code>fieldsummary</code> command calculates summary statistics for one or more fields in your events. The summary information is displayed as a results table.
- The fieldsummary command calculates summary statistics, such as the count, maximum value, minimum value, mean, and standard deviation for the fields in your search results. 

# Implementing searches
- You can create new KPIs in one of the two ways
    - Directly embed the selection, calculation, window and entity definitions into each KPI as you create them, or:
    - Define base searches that identify the selection, calculation, etc. first, and then use those when defining KPIs

# Base Searches
- If you have multiple KPIs that share a common source and schedule, you can combine them into base searches.
