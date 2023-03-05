# Key Performance Indicators

<h2>Introduction</h2>
For each service, define the KPIs that determine how well the service is performing.<br>
A KPI is a numeric measurement of a specific quantity that relates to the service’s function.<br>
For business services, KPIs are often measurements of targets or goals –Sales, quality, transactions, etc.<br>
For technical services, KPIs are usually metrics about devices or processes – CPU percentage, network load, etc.<br>

<b>Online sales</b>
<ul>
<li>Number of sold items</li>
<li>Total items ordered</li>
<li>Items viewed</li>
<li>Items returned</li>
</ul>

<b>Customer satisfaction</b>
<ul>
<li>Number of comments</li>
<li>Average rating</li>
</ul>

<b>Network</b>
<ul>
<li>Total traffic</li>
<li>Average latency</li>
<li>Number of nodes</li>
</ul>

<b>Web farm</b>
<ul>
<li>CPU utilization</li>
<li>Memory free</li>
<li>Storage free space</li>
</ul>

<h2> KPI Components</h2>

# Summary 
- Identify the service name and description
- For each KPI in the service, document its name, description, and:
    - Time span, update frequency and synchronization requirements
    - Entities? Split by entity?
    - Importance to the service health score
    - Threshold type: high, low or mid normal
- Identify team ownership, service templates, and service dependencies

# KPI Components

KPI gets its alert value (Alert_value) from: selected set of events, Calculatuions applied to field in the section, schedule, entity split settings. <br>

Additional KPI cobfigurations, importance, thresholds maps, synchronization and anomaly detection settings.<br>

# Entities 

- KPI should be split by entity, where the entities are the product lines or servers.<br>
- Some high-level KPIs will not map to entities.<br>
- Each KPI has an importance value, which defaults to 5 on a scale of 1 to 10 <br>
- If all the KPIs in a service have equal relevance to the overall service status, then you can leave the importance unchanged  <br>
- Some KPIs may be more important than others when calculating the service’s overall health  <br>
- If all the KPIs in a service have equal relevance to the overall service status, then you can leave the importance unchanged.<br>
- Some KPIs may be more important than others when calculating the service’s overall health.<br>

Example: the customer may say that “purchases are twice as important as other metrics”, so we set the importance of the Purchases KPI to 10 and leave others at 5. <br>

<b>Important / unimportant KPI</b>
2 special important settings <br>
- 0: KPI will not be used when calculating the service health score<br>
- 11: service health score cannot be better than this KPI’s alert severity<br>
    Example: the Online Sales service has a KPI, Purchases, which is arguably the most important factor impacting the overall service. If we set its importance to 11, the service health will never be better than the Purchases alert level.

# Thresholds
Thresholds are how ITSI converts a KPI’s numeric value into a status.<br>
Normal is “good”, critical is “bad”, with low, medium and high in between. <br>

