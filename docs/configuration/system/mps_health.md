#mps_health



Configuration for Health Monitoring Stats resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>disks_usage</td><td>&lt;mps_disk_usage[]></td><td>Read-write</td><td>Individual Disks Usage.</td></tr><tr><td>node_id</td><td>&lt;String></td><td>Read-write</td><td>Application Node ID.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>memory_total</td><td>&lt;Double></td><td>Read-only</td><td>Total memory in KB.</td></tr><tr><td>disk_total_capacity</td><td>&lt;Double></td><td>Read-only</td><td>Disk Total Capacity in KB.</td></tr><tr><td>disk_usage</td><td>&lt;Double></td><td>Read-only</td><td>Disk Usage (%).</td></tr><tr><td>disk_total</td><td>&lt;Double></td><td>Read-only</td><td>Total available disk space in KB.</td></tr><tr><td>memory_usage</td><td>&lt;Double></td><td>Read-only</td><td>Memory Usage (%).</td></tr><tr><td>disk_free</td><td>&lt;Double></td><td>Read-only</td><td>Free disk available in KB.</td></tr><tr><td>page_size</td><td>&lt;Double></td><td>Read-only</td><td>Total memory in KB.</td></tr><tr><td>memory_free</td><td>&lt;Double></td><td>Read-only</td><td>Free memory available in KB.</td></tr><tr><td>cpu_usage</td><td>&lt;Double></td><td>Read-only</td><td>CPU Usage (%).</td></tr><tr><td>disk_used</td><td>&lt;Double></td><td>Read-only</td><td>Disk used in KB.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_health

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_health":[{
"disks_usage":[{
"free_space":<Double_value>,
"parent_name":<String_value>,
"disk_usage":<Double_value>,
"used_space":<Double_value>,
"parent_id":<String_value>,
"disk_name":<String_value>,
"total_space":<Double_value>,
"disk_partition":<String_value>,
"disk_slice":<String_value>,
"id":<String_value>,
"disk_capacity":<Double_value>}],
"memory_total":<Double_value>,
"disk_total_capacity":<Double_value>,
"disk_usage":<Double_value>,
"disk_total":<Double_value>,
"memory_usage":<Double_value>,
"disk_free":<Double_value>,
"page_size":<Double_value>,
"node_id":<String_value>,
"memory_free":<Double_value>,
"cpu_usage":<Double_value>,
"id":<String_value>,
"disk_used":<Double_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_health/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_health":[{
"disks_usage":[{
"free_space":<Double_value>,
"parent_name":<String_value>,
"disk_usage":<Double_value>,
"used_space":<Double_value>,
"parent_id":<String_value>,
"disk_name":<String_value>,
"total_space":<Double_value>,
"disk_partition":<String_value>,
"disk_slice":<String_value>,
"id":<String_value>,
"disk_capacity":<Double_value>}],
"memory_total":<Double_value>,
"disk_total_capacity":<Double_value>,
"disk_usage":<Double_value>,
"disk_total":<Double_value>,
"memory_usage":<Double_value>,
"disk_free":<Double_value>,
"page_size":<Double_value>,
"node_id":<String_value>,
"memory_free":<Double_value>,
"cpu_usage":<Double_value>,
"id":<String_value>,
"disk_used":<Double_value>}]}
```







