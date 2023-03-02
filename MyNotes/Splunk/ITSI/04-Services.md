<h2> Services</h2>
You define <b>Services</b> which can analyse. Services is collection of IT objects that relates to your business goals.
<ol>
<li>Service is a Logical collection of objects</li>
<li>Services can be high level, business oriented or technical by nature</li>
<li>Service represents ex:a configurable item (CI) a funcational step or a business process </li>
</ol>

These services's health is determined by <b><i>Key Performance Indicators (KPI)</i></b> - Availablility, Performance, Latency, Durability.

KPI continuously moniters a health indicator for that respective services. Sum of KPI's result in the <i>service health score (0-100)</i> for each contribute according to their weight. 
Each KPI and the service health score is represented on a range of alert levels, ranging from inofrmation (Blue) to normal (green) to Critical (red). Both services & KPI's can be used as dependency.

Services can be High-level or low-level, tangible (Ex storage tier), Abstract, objects or group of people, dynamics & static.

# Service Design Process

<ol>
<li>Use customer requirements/glass table designs to identify services and KPIs</li>
<li>Coalesce KPIs into services</li>
<li>Identify related entities (server, devices, other)</li>
<li>Detailed KPI Planning - Importance (Weighting), Source events (data audit), Schedule, Thresholds</li>
<li>Map Inter-service dependencies</li>
</ol>

# Service-oriented Monitoring

segment the KPIs into logical groupings (services) that are related by business purpose, we can gain better understanding of the status of our critical processes.

<h2>Service Types</h2>
<ol>
<li><b>Business Services:</b> A business service is a system the organization needs to achieve
their goals</li>
<li><b>Technical Services:</b> is a physical system or resource the organization uses to accomplish the business services</li>
</ol>

# Scoping Services

- Consider the consumers (users) of each service: Do they care about a given KPI?<br>
- Relevancy: Do all the KPIs in a service relate to one identifiable system or process?<br>
- Reusability: Even if a set of KPIs does seem relevant, if they are also relevant to a
second service, they should be moved into a supporting service<br>

# Best Practices: Services
- Analyze the business to identify the most critical services<br>
- Ensure the services really apply to the site’s operations<br>
- Don’t get too focused on low-level services<br>
- Define a small number of key services first<br>
- Iteratively add more detail to your service descriptions and more services<br>