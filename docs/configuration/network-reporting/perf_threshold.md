#perf_threshold



Configuration for PerfThreshold resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sms_profile</td><td>&lt;String></td><td>Read-write</td><td>SMS Profile.</td></tr><tr><td>clear_message</td><td>&lt;String></td><td>Read-write</td><td>Clear Message.</td></tr><tr><td>threshold_type</td><td>&lt;String></td><td>Read-write</td><td>Threshold Type.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the perf thresholds configuration .<br>Maximum length = 256</td></tr><tr><td>report_name</td><td>&lt;String></td><td>Read-write</td><td>Report Name for which the threshold is configured.<br>Minimum length = 1<br>Maximum length = 100</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-write</td><td>Severity.</td></tr><tr><td>mail_profile</td><td>&lt;String></td><td>Read-write</td><td>Mail Profile.</td></tr><tr><td>tenant_name</td><td>&lt;String></td><td>Read-write</td><td>Tenant Name.</td></tr><tr><td>is_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>enabled or disabled.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family of which this threshold belongs to.</td></tr><tr><td>instances</td><td>&lt;String></td><td>Read-write</td><td>counter instances.<br>Minimum length = 1<br>Maximum length = 100</td></tr><tr><td>threshold_value</td><td>&lt;Double></td><td>Read-write</td><td>Threshold Value.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>duration</td><td>&lt;String></td><td>Read-write</td><td>duration of metric to be checked against threshold.</td></tr><tr><td>counter_name</td><td>&lt;String></td><td>Read-write</td><td>Counter Name for which the threshold is configured.<br>Minimum length = 1<br>Maximum length = 100</td></tr><tr><td>devices</td><td>&lt;String></td><td>Read-write</td><td>On which devices the threshold is enabled.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-write</td><td>Message.</td></tr><tr><td>clear_value</td><td>&lt;Double></td><td>Read-write</td><td>Clear Value.</td></tr><tr><td>devices_array</td><td>&lt;String[]></td><td>Read-write</td><td>Devices list.</td></tr><tr><td>instances_array</td><td>&lt;String[]></td><td>Read-write</td><td>Instances list.</td></tr><tr><td>clear_event</td><td>&lt;Boolean></td><td>Read-only</td><td>set to true if the event needs to be cleared.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_threshold?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{perf_threshold: {
"sms_profile":<String_value>,
"clear_message":<String_value>,
"devices_array":<String_value[]>,
"threshold_type":<String_value>,
"id":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"instances_array":<String_value[]>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_threshold":[{
"sms_profile":<String_value>,
"clear_message":<String_value>,
"threshold_type":<String_value>,
"clear_event":<Boolean_value>,
"id":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>,
"devices_array":<String_value>,
"instances_array":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_threshold/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_threshold

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_threshold":[{
"sms_profile":<String_value>,
"clear_message":<String_value>,
"threshold_type":<String_value>,
"clear_event":<Boolean_value>,
"id":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>,
"devices_array":<String_value>,
"instances_array":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_threshold/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_threshold":[{
"sms_profile":<String_value>,
"clear_message":<String_value>,
"threshold_type":<String_value>,
"clear_event":<Boolean_value>,
"id":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>,
"devices_array":<String_value>,
"instances_array":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_threshold/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{perf_threshold:{
<b>"id":<String_value></b>,
"sms_profile":<String_value>,
"clear_message":<String_value>,
"devices_array":<String_value[]>,
"threshold_type":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"instances_array":<String_value[]>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_threshold":[{
"sms_profile":<String_value>,
"clear_message":<String_value>,
"threshold_type":<String_value>,
"clear_event":<Boolean_value>,
"id":<String_value>,
"report_name":<String_value>,
"severity":<String_value>,
"mail_profile":<String_value>,
"tenant_name":<String_value>,
"is_enabled":<Boolean_value>,
"device_family":<String_value>,
"instances":<String_value>,
"threshold_value":<Double_value>,
"name":<String_value>,
"duration":<String_value>,
"counter_name":<String_value>,
"devices":<String_value>,
"message":<String_value>,
"clear_value":<Double_value>,
"devices_array":<String_value>,
"instances_array":<String_value>}]}
```







