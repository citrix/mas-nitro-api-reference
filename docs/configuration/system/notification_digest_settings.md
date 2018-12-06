#notification_digest_settings



Configuration for Notification Digest Settings resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>WeeklyFeaturesList</td><td>&lt;String></td><td>Read-write</td><td>List of events for which notification is to be generated weekly..</td></tr><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>scheduleOptions</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated Options for scheduling Configuration Template.</td></tr><tr><td>ImmediateFeaturesList</td><td>&lt;String></td><td>Read-write</td><td>List of events for which notification is to be generated immediately..</td></tr><tr><td>MonthlyFeaturesList</td><td>&lt;String></td><td>Read-write</td><td>List of events for which notification is to be generated monthly..</td></tr><tr><td>nextScheduleTimeEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch at which job is scheduled to be run next..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated for each setting.</td></tr><tr><td>DailyFeaturesList</td><td>&lt;String></td><td>Read-write</td><td>List of events for which notification is to be generated daily..</td></tr><tr><td>notification_period</td><td>&lt;String></td><td>Read-write</td><td>notification_period.</td></tr><tr><td>mail_profile</td><td>&lt;String></td><td>Read-write</td><td>Mail Profile.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id of the Notification Jobs.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/notification_digest_settings?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{notification_digest_settings: {
"WeeklyFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"id":<String_value>,
"DailyFeaturesList":<String_value>,
"mail_profile":<String_value>,
"notification_period":<String_value>,
"scheduleTimesEpoch":<String_value>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"ImmediateFeaturesList":<String_value>,
"nextScheduleTimeEpoch":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "notification_digest_settings":[{
"WeeklyFeaturesList":<String_value>,
"scheduleTimesEpoch":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"ImmediateFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"tenant_id":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"id":<String_value>,
"DailyFeaturesList":<String_value>,
"notification_period":<String_value>,
"mail_profile":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/notification_digest_settings/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/notification_digest_settings

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "notification_digest_settings":[{
"WeeklyFeaturesList":<String_value>,
"scheduleTimesEpoch":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"ImmediateFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"tenant_id":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"id":<String_value>,
"DailyFeaturesList":<String_value>,
"notification_period":<String_value>,
"mail_profile":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/notification_digest_settings/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "notification_digest_settings":[{
"WeeklyFeaturesList":<String_value>,
"scheduleTimesEpoch":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"ImmediateFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"tenant_id":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"id":<String_value>,
"DailyFeaturesList":<String_value>,
"notification_period":<String_value>,
"mail_profile":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/notification_digest_settings/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{notification_digest_settings:{
<b>"id":<String_value></b>,
<b>"notification_period":<String_value></b>,
"WeeklyFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"DailyFeaturesList":<String_value>,
"mail_profile":<String_value>,
"scheduleTimesEpoch":<String_value>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"ImmediateFeaturesList":<String_value>,
"nextScheduleTimeEpoch":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "notification_digest_settings":[{
"WeeklyFeaturesList":<String_value>,
"scheduleTimesEpoch":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"ImmediateFeaturesList":<String_value>,
"MonthlyFeaturesList":<String_value>,
"tenant_id":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"id":<String_value>,
"DailyFeaturesList":<String_value>,
"notification_period":<String_value>,
"mail_profile":<String_value>}]}
```







