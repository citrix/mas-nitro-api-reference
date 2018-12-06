#ns_event



Configuration for NetScalerEvent resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>counter_threshold_value</td><td>&lt;String></td><td>Read-write</td><td>device threshold value for any threadhold violated traps.</td></tr><tr><td>cmd_exec_status</td><td>&lt;String></td><td>Read-write</td><td>Command Execution Status.<br>Maximum length = 255</td></tr><tr><td>device_entity_type</td><td>&lt;String></td><td>Read-write</td><td>Device Entity Type.<br>Maximum length = 255</td></tr><tr><td>device_type</td><td>&lt;String></td><td>Read-write</td><td>Device Type.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the events.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>user_name</td><td>&lt;String></td><td>Read-write</td><td>Username.<br>Maximum length = 255</td></tr><tr><td>config_cmd</td><td>&lt;String></td><td>Read-write</td><td>Config Command.</td></tr><tr><td>cmd_auth_status</td><td>&lt;String></td><td>Read-write</td><td>Command Authorization Status.<br>Maximum length = 255</td></tr><tr><td>device_entity_name</td><td>&lt;String></td><td>Read-write</td><td>Device Entity Name.</td></tr><tr><td>counter_actual_value</td><td>&lt;String></td><td>Read-write</td><td>device actual value for any threadhold violated traps.</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Assign hostname to managed device, if this is not provided, name will be set as host name .<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>source</td><td>&lt;String></td><td>Read-only</td><td>Source.</td></tr><tr><td>entity</td><td>&lt;String></td><td>Read-only</td><td>Entity of Event.</td></tr><tr><td>timestamp</td><td>&lt;Integer></td><td>Read-only</td><td>Event Time.</td></tr><tr><td>operation_type</td><td>&lt;String></td><td>Read-only</td><td>Operation Type.</td></tr><tr><td>category</td><td>&lt;String></td><td>Read-only</td><td>Category of Event.</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-only</td><td>Severity of Event.</td></tr><tr><td>failureobj</td><td>&lt;String></td><td>Read-only</td><td>Failure Object.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-only</td><td>Event Message.</td></tr><tr><td>current_value</td><td>&lt;String></td><td>Read-only</td><td>Current Value, cab be used while sending traps.</td></tr><tr><td>threshold_value</td><td>&lt;String></td><td>Read-only</td><td>Threshold Value, cab be used while sending traps.</td></tr><tr><td>entity_type</td><td>&lt;String></td><td>Read-only</td><td>Entity Type.</td></tr><tr><td>matched_filters</td><td>&lt;String></td><td>Read-only</td><td>Matched Event Filter Ids separated by comma.</td></tr><tr><td>managed_device_id</td><td>&lt;String></td><td>Read-only</td><td>Managed Device ID.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_event

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_event":[{
"counter_threshold_value":<String_value>,
"source":<String_value>,
"cmd_exec_status":<String_value>,
"device_entity_type":<String_value>,
"entity":<String_value>,
"device_type":<String_value>,
"timestamp":<Integer_value>,
"operation_type":<String_value>,
"id":<String_value>,
"category":<String_value>,
"severity":<String_value>,
"failureobj":<String_value>,
"device_family":<String_value>,
"rpt_sample_time":<Double_value>,
"message":<String_value>,
"user_name":<String_value>,
"config_cmd":<String_value>,
"cmd_auth_status":<String_value>,
"device_entity_name":<String_value>,
"counter_actual_value":<String_value>,
"current_value":<String_value>,
"threshold_value":<String_value>,
"entity_type":<String_value>,
"hostname":<String_value>,
"matched_filters":<String_value>,
"managed_device_id":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_event/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_event":[{
"counter_threshold_value":<String_value>,
"source":<String_value>,
"cmd_exec_status":<String_value>,
"device_entity_type":<String_value>,
"entity":<String_value>,
"device_type":<String_value>,
"timestamp":<Integer_value>,
"operation_type":<String_value>,
"id":<String_value>,
"category":<String_value>,
"severity":<String_value>,
"failureobj":<String_value>,
"device_family":<String_value>,
"rpt_sample_time":<Double_value>,
"message":<String_value>,
"user_name":<String_value>,
"config_cmd":<String_value>,
"cmd_auth_status":<String_value>,
"device_entity_name":<String_value>,
"counter_actual_value":<String_value>,
"current_value":<String_value>,
"threshold_value":<String_value>,
"entity_type":<String_value>,
"hostname":<String_value>,
"matched_filters":<String_value>,
"managed_device_id":<String_value>}]}
```







