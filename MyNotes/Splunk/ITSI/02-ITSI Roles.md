# Roles

<ol>
<li><b>itoa_user:</b> View most of ITSI, create private glass tables or deep dives. Access shared views (analyzers, deep dives, glass tables); modify default glass tables, create private views, own notable event episodes </li>
<li><b>itoa_analyst:</b> itoa_user + own notable events, modify default service analyzers,
and share new views</li>
<li><b>itoa_team_admin:</b> itoa_analyst, create shared services, KPI's  entities for the team. </li>
<li><b>itoa_admin:</b>itoa_team_analyst + bulk imports entities/services, read/write/delete backup and restores and manage all other objects</li>
<li><b>itoa_team_admin:</b> The itoa_team_admin role is assigned to users who will own services that belong to specific teams.</li>
</ol>

Additional roles can be created as needed.<br>

The admin role on ITSI search heads should inherit from <b> itoa_admin </b> to provide full access to all ITSI object types<br>