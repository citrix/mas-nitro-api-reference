#ns_configtemplate_scheduler



Configuration for config audit template scheduler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Epoch times for scheduling the job.</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>Name of object which is adding this resource as embedded object .</td></tr><tr><td>daily_time</td><td>&lt;String></td><td>Read-write</td><td>Daily time details of scheduler.</td></tr><tr><td>recurrenceOptions</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated recurrence options of job that is scheduled.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the events.</td></tr><tr><td>recurrence_type</td><td>&lt;String></td><td>Read-write</td><td>Daily, Week or Monthly option.<br>Maximum length = 255</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>Parent id of object which is adding this resource as embedded object .</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate_scheduler?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate_scheduler: {
"parent_id":<String_value>,
"id":<String_value>,
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"recurrenceOptions":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate_scheduler":[{
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrenceOptions":<String_value>,
"id":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"parent_id":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate_scheduler/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate_scheduler

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate_scheduler":[{
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrenceOptions":<String_value>,
"id":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"parent_id":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate_scheduler/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate_scheduler":[{
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrenceOptions":<String_value>,
"id":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"parent_id":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate_scheduler/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate_scheduler:{
<b>"id":<String_value></b>,
"parent_id":<String_value>,
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"recurrenceOptions":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate_scheduler":[{
"scheduleTimesEpoch":<String_value>,
"parent_name":<String_value>,
"daily_time":<String_value>,
"recurrenceOptions":<String_value>,
"id":<String_value>,
"recurrence_type":<String_value>,
"tz_offset":<Integer_value>,
"parent_id":<String_value>}]}
```







