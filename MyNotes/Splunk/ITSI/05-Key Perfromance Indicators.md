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

# Permission
- Services are owned by teams. <br>
- There is one default global team which contains all ITSI users, so by default all users can use any service. <br>
- If needed, you can create new teams and use them to restrict access to some services.<br>
- Each team has an administrative role assigned to it, inherited from itoa_team_admin. <br>

# Dependency 
- A service can depend on other services. <br>
- Dependency can be one or more KPIs in another service. The health score of another services. <br>
- During design, periodically examine your services. <br>

# Service Templates
- You may find that you have several discrete services that are identical in structure. <br>
- You can design one service template as an abstract description of a type of service. <br>
- Then you can implement new services from the template as needed.  <br>