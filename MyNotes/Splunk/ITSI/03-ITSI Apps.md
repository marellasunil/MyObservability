# ITSI Apps Installatiuon & Configurations

<h2>ITSI App components</h2>
Component location - Search heads<br>
    DA-ITSI-APPSERVER : Domain add-ons Modules<br>
    DA-ITSI-DATABASE : Domain add-ons Modules<br>
    DA-ITSI-EUEM : Domain add-ons Modules<br>
    DA-ITSI-LB : Domain add-ons Modules<br>
    DA-ITSI-OS : Domain add-ons Modules<br>
    DA-ITSI-STORAGE : Domain add-ons Modules<br>
    DA-ITSI-VIRTUALIZATION : Domain add-ons Modules<br>
    DA-ITSI-WEBSERVER : Domain add-ons Modules<br>
    SA-ITOA: Entity and service management<br>
    SA-ITSI-ATAD: Adaptive threshold management<br>
    SA-ITSI-CustomModuleViz: Custom visualization files<br>
    SA-ITSI-MetricAD: Anomaly detection tools and services<br>
<br>
Component location - Search heads, License Master<br>
    SA-ITSI-Licensechecker: Validate ITSI licenses<br>
    SA-ITOA<br>
    SA-UserAccess: ITSI access control tools<br>
<br>
Component location - Search heads, Indexers<br>
    SA-IndexCreation: ITSI summary index configurations<br>

<h2>ITSI Indexes</h2>
Created on indexers by SA-IndexCreation<br>
<br>
anomaly_detection : AD alert storage<br>
itsi_grouped_alerts : Metadata for incident review<br>
itsi_notable_archive : Old incident review data<br>
itsi_notable_audit : Incident review management<br>
itsi_summary : KPI storage<br>
itsi_tracked_alerts : Incident review alert data<br>
snmptrapd : SNMP correlation search data<br>

<h2>ITSI Apps Installation Procedure</h2>
<ol>
<li>Extract apps in etc/apps. If it is SH Cluster, etc/shcluster/apps</li>
<li>Copy SA-IndexCreation to the indexers, If it is indexer cluster, Copy SA-IndexCreation to the etc/master-apps/ directory on cluster master node</li></li>
<li>Copy SA-ITSI-Licensechecker, SA-ITOA and SA-UserAccess to the license master</li>
<li>if it is SH Cluster, <code>splunk apply shcluster-bundle</code></li>
<li>If it is indexer cluster, <code>splunk apply cluster-bundle</code></li>
<li>Restart Splunk on all servers. Rolling restart if it is SH Cluster</li>
</ol>
Note: Remove SA-ITSI-Licensechecker from non-license master servers