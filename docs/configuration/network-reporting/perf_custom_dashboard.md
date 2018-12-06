#perf_custom_dashboard



Configuration for PerfCustomDashboard resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family of which this custom dashboard belongs to.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Custom dashboard description.</td></tr><tr><td>timestamp</td><td>&lt;Double></td><td>Read-write</td><td>timestamp in seconds.</td></tr><tr><td>entity_type</td><td>&lt;String></td><td>Read-write</td><td>Entity Type.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the perf custom dashboard configuration .<br>Maximum length = 256</td></tr><tr><td>entities_array</td><td>&lt;String[]></td><td>Read-write</td><td>Entities (Virtual servers or Network Interfaces).</td></tr><tr><td>coordinates_array</td><td>&lt;String[]></td><td>Read-write</td><td>Co-ordinates in array.</td></tr><tr><td>instances_array</td><td>&lt;String[]></td><td>Read-write</td><td>Instances in array.</td></tr><tr><td>report_names_array</td><td>&lt;String[]></td><td>Read-write</td><td>Report names in array.</td></tr><tr><td>report_names</td><td>&lt;String></td><td>Read-only</td><td>Report Names.</td></tr><tr><td>coordinates</td><td>&lt;String></td><td>Read-only</td><td>Co-ordinates.</td></tr><tr><td>instances</td><td>&lt;String></td><td>Read-only</td><td>Instances.</td></tr><tr><td>entities</td><td>&lt;String></td><td>Read-only</td><td>Entities(virtual servers or network interfaces).</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_custom_dashboard?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{perf_custom_dashboard: {
"report_names_array":<String_value[]>,
"id":<String_value>,
"entities_array":<String_value[]>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"coordinates_array":<String_value[]>,
"instances_array":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_custom_dashboard":[{
"report_names":<String_value>,
"coordinates":<String_value>,
"instances":<String_value>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"entities":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"id":<String_value>,
"entities_array":<String_value>,
"coordinates_array":<String_value>,
"instances_array":<String_value>,
"report_names_array":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_custom_dashboard/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_custom_dashboard

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_custom_dashboard":[{
"report_names":<String_value>,
"coordinates":<String_value>,
"instances":<String_value>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"entities":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"id":<String_value>,
"entities_array":<String_value>,
"coordinates_array":<String_value>,
"instances_array":<String_value>,
"report_names_array":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_custom_dashboard/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_custom_dashboard":[{
"report_names":<String_value>,
"coordinates":<String_value>,
"instances":<String_value>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"entities":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"id":<String_value>,
"entities_array":<String_value>,
"coordinates_array":<String_value>,
"instances_array":<String_value>,
"report_names_array":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_custom_dashboard/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{perf_custom_dashboard:{
<b>"id":<String_value></b>,
"report_names_array":<String_value[]>,
"entities_array":<String_value[]>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"coordinates_array":<String_value[]>,
"instances_array":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_custom_dashboard":[{
"report_names":<String_value>,
"coordinates":<String_value>,
"instances":<String_value>,
"device_family":<String_value>,
"name":<String_value>,
"description":<String_value>,
"entities":<String_value>,
"timestamp":<Double_value>,
"entity_type":<String_value>,
"id":<String_value>,
"entities_array":<String_value>,
"coordinates_array":<String_value>,
"instances_array":<String_value>,
"report_names_array":<String_value>}]}
```







