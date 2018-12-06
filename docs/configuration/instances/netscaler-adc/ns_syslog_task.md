#ns_syslog_task



Configuration for NS Syslog Configure Task resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Family of Devices for which config template is defined..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>device_groups</td><td>&lt;String[]></td><td>Read-write</td><td>Device Group Array on which for which template is applied.</td></tr><tr><td>scheduleTimes</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated times of the day(HH:MM) on which Configuration Template is scheduled.</td></tr><tr><td>variables</td><td>&lt;variable_values[]></td><td>Read-write</td><td>Values of Variables used in commands of the configuration template.</td></tr><tr><td>on_error</td><td>&lt;String></td><td>Read-write</td><td>Behaviour on encountering error while applying configuration template on a device: CONTINUE|EXIT.<br>Minimum length = 1<br>Maximum length = 16</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Syslog server port.<br>Maximum value =</td></tr><tr><td>execute_sequentially</td><td>&lt;Boolean></td><td>Read-write</td><td>True if configuration template is to be applied to devices sequentially.</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>scheduleOptions</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated Options for scheduling Configuration Template.</td></tr><tr><td>devices</td><td>&lt;String[]></td><td>Read-write</td><td>Device IP Address Array on which template is applied.</td></tr><tr><td>scheduleType</td><td>&lt;String></td><td>Read-write</td><td>Schedule Type of Configuration Template that is scheduled.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>Syslog server IP address.<br>Minimum length = 1<br>Maximum length = 64</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_task?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_syslog_task: {
<b>"port":<Integer_value></b>,
<b>"ip_address":<String_value></b>,
"scheduleTimes":<String_value>,
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"id":<String_value>,
"device":<String_value>,
"device_group":<String_value>,
"parent_id":<String_value>}],
"default_value":<String_value>,
"id":<String_value>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"execute_sequentially":<Boolean_value>,
"scheduleTimesEpoch":<String_value>,
"device_groups":<String_value[]>,
"device_family":<String_value>,
"on_error":<String_value>,
"devices":<String_value[]>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"scheduleType":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_syslog_task":[{
"scheduleTimesEpoch":<String_value>,
"device_family":<String_value>,
"device_groups":<String_value>,
"scheduleTimes":<String_value>,
"variables":[{
"device_values_mapping":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"id":<String_value>,
"device_group":<String_value>,
"device":<String_value>,
"parent_id":<String_value>}],
"parent_id":<String_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>}],
"on_error":<String_value>,
"port":<Integer_value>,
"execute_sequentially":<Boolean_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"devices":<String_value>,
"scheduleType":<String_value>,
"ip_address":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_task/

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_task

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_syslog_task":[{
"scheduleTimesEpoch":<String_value>,
"device_family":<String_value>,
"device_groups":<String_value>,
"scheduleTimes":<String_value>,
"variables":[{
"device_values_mapping":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"id":<String_value>,
"device_group":<String_value>,
"device":<String_value>,
"parent_id":<String_value>}],
"parent_id":<String_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>}],
"on_error":<String_value>,
"port":<Integer_value>,
"execute_sequentially":<Boolean_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"devices":<String_value>,
"scheduleType":<String_value>,
"ip_address":<String_value>}]}
```







