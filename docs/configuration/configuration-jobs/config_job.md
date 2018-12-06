#config_job



Configuration for Configuration Job resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>scheduleTimes</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated times of the day(HH:MM) on which Configuration Template is scheduled.</td></tr><tr><td>sms_profiles</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of SMS profiles.</td></tr><tr><td>execute_sequentially</td><td>&lt;Boolean></td><td>Read-write</td><td>True if configuration template is to be applied to devices sequentially.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the configuration jobs.</td></tr><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>credentials_required</td><td>&lt;Boolean></td><td>Read-write</td><td>True if username/password need to be asked before configuration template is to applied on devices.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Family of Devices for which config job was executed.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>tasklog_id</td><td>&lt;String></td><td>Read-write</td><td>Task Log Id of the Config Job.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of configuration job.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>template_info</td><td>&lt;configuration_template></td><td>Read-write</td><td>Configuration Template to be executed/scheduled.</td></tr><tr><td>on_error</td><td>&lt;String></td><td>Read-write</td><td>Behaviour on encountering error while applying configuration template on a device: CONTINUE|EXIT|ROLLBACK.<br>Minimum length = 1<br>Maximum length = 16</td></tr><tr><td>devices</td><td>&lt;String[]></td><td>Read-write</td><td>Device IP Address Array on which job is run.</td></tr><tr><td>scheduleOptions</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated Options for scheduling Configuration Template.</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>mail_profiles</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of Mail profiles.</td></tr><tr><td>device_groups_db</td><td>&lt;String></td><td>Read-write</td><td>Device Groups List Comma Seperated on which job is run.</td></tr><tr><td>execute_username</td><td>&lt;String></td><td>Read-write</td><td>Execute User Name for job.<br>Maximum length = 127</td></tr><tr><td>variables</td><td>&lt;config_variable[]></td><td>Read-write</td><td>Values of Variables used in commands of the configuration template.</td></tr><tr><td>lastExecutedTimeEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch at which job was last executed..</td></tr><tr><td>execute_batch</td><td>&lt;Boolean></td><td>Read-write</td><td>True if config job commands execute as batch.</td></tr><tr><td>node_id</td><td>&lt;String></td><td>Read-write</td><td>Node id of the node executing the task in a Multinode / HA deployment.</td></tr><tr><td>execute_password</td><td>&lt;String></td><td>Read-write</td><td>Execute Password for job.<br>Maximum length = 127</td></tr><tr><td>devices_db</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address List Comma Seperated on which job is run.</td></tr><tr><td>device_groups</td><td>&lt;String[]></td><td>Read-write</td><td>Device Group Array on which for which job is run.</td></tr><tr><td>scheduleType</td><td>&lt;String></td><td>Read-write</td><td>Schedule Type of Configuration Template that is scheduled.</td></tr><tr><td>nextScheduleTimeEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch at which job is scheduled to be run next..</td></tr><tr><td>preview_commands</td><td>&lt;String[]></td><td>Read-write</td><td>Preview of list of commands.</td></tr><tr><td>preview_rollback_commands</td><td>&lt;String[]></td><td>Read-write</td><td>Preview of list of rollback commands.</td></tr><tr><td>executed_by</td><td>&lt;String></td><td>Read-only</td><td>Name of user who executed configuration job.</td></tr><tr><td>lastExecutionStatus</td><td>&lt;String></td><td>Read-only</td><td>Status of last Execution of Config Job.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>Name of user who created configuration job.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of Config Job.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id of the Config Jobs.</td></tr><tr><td>timestamp</td><td>&lt;Integer></td><td>Read-only</td><td>Time of Creation of Configuration Job.</td></tr><tr><td>devices_count</td><td>&lt;Integer></td><td>Read-only</td><td>Number of Devices on which commands executed.</td></tr><tr><td>devices_completed_count</td><td>&lt;Integer></td><td>Read-only</td><td>Devices Completed Count.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/config_job?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{config_job: {
"scheduleTimes":<String_value>,
"sms_profiles":<String_value>,
"execute_sequentially":<Boolean_value>,
"preview_rollback_commands":<String_value[]>,
"id":<String_value>,
"credentials_required":<Boolean_value>,
"scheduleTimesEpoch":<String_value>,
"device_family":<String_value>,
"tasklog_id":<String_value>,
"name":<String_value>,
"template_info":<configuration_template_value>,
"on_error":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"devices":<String_value[]>,
"device_groups_db":<String_value>,
"mail_profiles":<String_value>,
"execute_username":<String_value>,
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"device":<String_value>,
"device_group":<String_value>,
"parent_id":<String_value>,
"id":<String_value>}],
"default_value":<String_value>,
"id":<String_value>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"execute_batch":<Boolean_value>,
"lastExecutedTimeEpoch":<String_value>,
"execute_password":<String_value>,
"node_id":<String_value>,
"devices_db":<String_value>,
"device_groups":<String_value[]>,
"scheduleType":<String_value>,
"preview_commands":<String_value[]>,
"nextScheduleTimeEpoch":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "config_job":[{
"scheduleTimes":<String_value>,
"sms_profiles":<String_value>,
"execute_sequentially":<Boolean_value>,
"id":<String_value>,
"executed_by":<String_value>,
"lastExecutionStatus":<String_value>,
"scheduleTimesEpoch":<String_value>,
"credentials_required":<Boolean_value>,
"device_family":<String_value>,
"tasklog_id":<String_value>,
"name":<String_value>,
"template_info":<configuration_template_value>,
"on_error":<String_value>,
"devices":<String_value>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"username":<String_value>,
"mail_profiles":<String_value>,
"device_groups_db":<String_value>,
"execute_username":<String_value>,
"status":<String_value>,
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
"tenant_id":<String_value>,
"lastExecutedTimeEpoch":<String_value>,
"execute_batch":<Boolean_value>,
"timestamp":<Integer_value>,
"node_id":<String_value>,
"execute_password":<String_value>,
"devices_db":<String_value>,
"device_groups":<String_value>,
"scheduleType":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"preview_commands":<String_value>,
"preview_rollback_commands":<String_value>,
"devices_count":<Integer_value>,
"devices_completed_count":<Integer_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/config_job/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/config_job

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "config_job":[{
"scheduleTimes":<String_value>,
"sms_profiles":<String_value>,
"execute_sequentially":<Boolean_value>,
"id":<String_value>,
"executed_by":<String_value>,
"lastExecutionStatus":<String_value>,
"scheduleTimesEpoch":<String_value>,
"credentials_required":<Boolean_value>,
"device_family":<String_value>,
"tasklog_id":<String_value>,
"name":<String_value>,
"template_info":<configuration_template_value>,
"on_error":<String_value>,
"devices":<String_value>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"username":<String_value>,
"mail_profiles":<String_value>,
"device_groups_db":<String_value>,
"execute_username":<String_value>,
"status":<String_value>,
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
"tenant_id":<String_value>,
"lastExecutedTimeEpoch":<String_value>,
"execute_batch":<Boolean_value>,
"timestamp":<Integer_value>,
"node_id":<String_value>,
"execute_password":<String_value>,
"devices_db":<String_value>,
"device_groups":<String_value>,
"scheduleType":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"preview_commands":<String_value>,
"preview_rollback_commands":<String_value>,
"devices_count":<Integer_value>,
"devices_completed_count":<Integer_value>}]}
```







###modify







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/config_job/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{config_job:{
<b>"id":<String_value></b>,
"scheduleTimes":<String_value>,
"sms_profiles":<String_value>,
"execute_sequentially":<Boolean_value>,
"preview_rollback_commands":<String_value[]>,
"credentials_required":<Boolean_value>,
"scheduleTimesEpoch":<String_value>,
"device_family":<String_value>,
"tasklog_id":<String_value>,
"name":<String_value>,
"template_info":<configuration_template_value>,
"on_error":<String_value>,
"tz_offset":<Integer_value>,
"scheduleOptions":<String_value>,
"devices":<String_value[]>,
"device_groups_db":<String_value>,
"mail_profiles":<String_value>,
"execute_username":<String_value>,
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"device":<String_value>,
"device_group":<String_value>,
"parent_id":<String_value>,
"id":<String_value>}],
"default_value":<String_value>,
"id":<String_value>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"execute_batch":<Boolean_value>,
"lastExecutedTimeEpoch":<String_value>,
"execute_password":<String_value>,
"node_id":<String_value>,
"devices_db":<String_value>,
"device_groups":<String_value[]>,
"scheduleType":<String_value>,
"preview_commands":<String_value[]>,
"nextScheduleTimeEpoch":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "config_job":[{
"scheduleTimes":<String_value>,
"sms_profiles":<String_value>,
"execute_sequentially":<Boolean_value>,
"id":<String_value>,
"executed_by":<String_value>,
"lastExecutionStatus":<String_value>,
"scheduleTimesEpoch":<String_value>,
"credentials_required":<Boolean_value>,
"device_family":<String_value>,
"tasklog_id":<String_value>,
"name":<String_value>,
"template_info":<configuration_template_value>,
"on_error":<String_value>,
"devices":<String_value>,
"scheduleOptions":<String_value>,
"tz_offset":<Integer_value>,
"username":<String_value>,
"mail_profiles":<String_value>,
"device_groups_db":<String_value>,
"execute_username":<String_value>,
"status":<String_value>,
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
"tenant_id":<String_value>,
"lastExecutedTimeEpoch":<String_value>,
"execute_batch":<Boolean_value>,
"timestamp":<Integer_value>,
"node_id":<String_value>,
"execute_password":<String_value>,
"devices_db":<String_value>,
"device_groups":<String_value>,
"scheduleType":<String_value>,
"nextScheduleTimeEpoch":<String_value>,
"preview_commands":<String_value>,
"preview_rollback_commands":<String_value>,
"devices_count":<Integer_value>,
"devices_completed_count":<Integer_value>}]}
```







