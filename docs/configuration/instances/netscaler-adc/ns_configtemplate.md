#ns_configtemplate



Configuration for NetScaler configuration template resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>to_be_exported</td><td>&lt;Boolean></td><td>Read-write</td><td>Setting for enabling/disabling config audit diff report.</td></tr><tr><td>variable_vals</td><td>&lt;variable_values[]></td><td>Read-write</td><td>Values of Variables used in commands of the audit template.</td></tr><tr><td>isDefaultSchedule</td><td>&lt;Boolean></td><td>Read-write</td><td>Scheduled specification for template or default polling interval.</td></tr><tr><td>commands</td><td>&lt;ns_command[]></td><td>Read-write</td><td>NS Configuration Commands.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the configuration template.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>variables</td><td>&lt;config_variable[]></td><td>Read-write</td><td>Array of variables used in commands of the configuration template.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Template Description.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>scheduleDetail</td><td>&lt;String></td><td>Read-write</td><td>Schedule Detail.</td></tr><tr><td>device_groups_db</td><td>&lt;String></td><td>Read-write</td><td>Device Groups List Comma Seperated to store in DB.</td></tr><tr><td>last_updated_time</td><td>&lt;Integer></td><td>Read-write</td><td>Last Updated Time.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>template_file</td><td>&lt;String></td><td>Read-write</td><td>Template File that is to be imported.</td></tr><tr><td>scheduleInfo</td><td>&lt;ns_configtemplate_scheduler></td><td>Read-write</td><td>Scheduling information for audit template.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the system users.</td></tr><tr><td>mail_profile</td><td>&lt;String></td><td>Read-write</td><td>Mail profile name to send notification mail..<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>preview_commands</td><td>&lt;String[]></td><td>Read-write</td><td>Preview of list of commands.</td></tr><tr><td>device_groups</td><td>&lt;String[]></td><td>Read-write</td><td>Device Group Array for which audit template is added.</td></tr><tr><td>devices</td><td>&lt;String[]></td><td>Read-write</td><td>List of NS IP Address.</td></tr><tr><td>template_create_user</td><td>&lt;String></td><td>Read-only</td><td>User who created the template.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[IMPORT_VARIABLES_FILE](#import_variables)| [ADD](#add)| [PREVIEW](#pr)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###import_variables_file







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate?action=import_variables_file;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate: {
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"commands":[{
<b>"id":<String_value></b>,
"parent_id":<String_value>,
"command":<String_value>,
"parent_name":<String_value>}],
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum":<String_value[]>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"scheduleDetail":<String_value>,
"last_updated_time":<Integer_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"device_groups":<String_value[]>,
"isDefaultSchedule":<Boolean_value>,
"name":<String_value>,
"description":<String_value>,
"devices":<String_value[]>,
"device_groups_db":<String_value>,
"preview_commands":<String_value[]>,
"scheduleInfo":<ns_configtemplate_scheduler_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate: {
<b>"commands":[{
<b>"id":<String_value></b>,
"parent_id":<String_value>,
"command":<String_value>,
"parent_name":<String_value>}]</b>,
<b>"name":<String_value></b>,
<b>"devices":<String_value[]></b>,
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum":<String_value[]>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"scheduleDetail":<String_value>,
"last_updated_time":<Integer_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"device_groups":<String_value[]>,
"isDefaultSchedule":<Boolean_value>,
"description":<String_value>,
"device_groups_db":<String_value>,
"preview_commands":<String_value[]>,
"scheduleInfo":<ns_configtemplate_scheduler_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







###preview







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate?action=preview;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate: {
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"commands":[{
<b>"id":<String_value></b>,
"parent_id":<String_value>,
"command":<String_value>,
"parent_name":<String_value>}],
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum":<String_value[]>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"scheduleDetail":<String_value>,
"last_updated_time":<Integer_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"device_groups":<String_value[]>,
"isDefaultSchedule":<Boolean_value>,
"name":<String_value>,
"description":<String_value>,
"devices":<String_value[]>,
"device_groups_db":<String_value>,
"preview_commands":<String_value[]>,
"scheduleInfo":<ns_configtemplate_scheduler_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







###modify







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_configtemplate/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_configtemplate:{
<b>"commands":[{
<b>"id":<String_value></b>,
"parent_id":<String_value>,
"command":<String_value>,
"parent_name":<String_value>}]</b>,
<b>"id":<String_value></b>,
<b>"devices":<String_value[]></b>,
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum":<String_value[]>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"description":<String_value>,
"display_name":<String_value>,
"type":<String_value>}],
"scheduleDetail":<String_value>,
"last_updated_time":<Integer_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"mail_profile":<String_value>,
"device_groups":<String_value[]>,
"isDefaultSchedule":<Boolean_value>,
"name":<String_value>,
"description":<String_value>,
"device_groups_db":<String_value>,
"preview_commands":<String_value[]>,
"scheduleInfo":<ns_configtemplate_scheduler_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_configtemplate":[{
"to_be_exported":<Boolean_value>,
"variable_vals":[{
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
"isDefaultSchedule":<Boolean_value>,
"devicelistCombined":<String_value>,
"commands":[{
"index":<Integer_value>,
"parent_name":<String_value>,
"id":<String_value>,
"command":<String_value>,
"parent_id":<String_value>}],
"name":<String_value>,
"variables":[{
"parent_name":<String_value>,
"name":<String_value>,
"display_name":<String_value>,
"description":<String_value>,
"parent_id":<String_value>,
"required":<Boolean_value>,
"default_value":<String_value>,
"id":<String_value>,
"type":<String_value>,
"values_enum_db":<String_value>,
"values_enum":<String_value>}],
"devicelist":<String_value>,
"description":<String_value>,
"scheduleDetail":<String_value>,
"device_groups_db":<String_value>,
"last_updated_time":<Integer_value>,
"template_create_user":<String_value>,
"tenant_id":<String_value>,
"template_file":<String_value>,
"scheduleInfo":<ns_configtemplate_scheduler_value>,
"id":<String_value>,
"mail_profile":<String_value>,
"preview_commands":<String_value>,
"device_groups":<String_value>,
"devices":<String_value>}]}
```







