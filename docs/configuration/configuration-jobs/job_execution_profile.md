#job_execution_profile



Configuration for Job Execution Profile resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>job_name</td><td>&lt;String></td><td>Read-write</td><td>Job Name.</td></tr><tr><td>variables</td><td>&lt;eventrule_config_variable[]></td><td>Read-write</td><td>Values of Variables used in commands of the configuration template.</td></tr><tr><td>template_info</td><td>&lt;eventrule_configuration_template></td><td>Read-write</td><td>Configuration Template to be executed/scheduled.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the job profile..</td></tr><tr><td>on_error</td><td>&lt;String></td><td>Read-write</td><td>Behaviour on encountering error while applying configuration template on a device: CONTINUE|EXIT|ROLLBACK.<br>Minimum length = 1<br>Maximum length = 16</td></tr><tr><td>instance_type</td><td>&lt;String></td><td>Read-write</td><td>Instance Type.</td></tr><tr><td>profile_name</td><td>&lt;String></td><td>Read-write</td><td>Profile name for the job setting..<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id .</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/job_execution_profile?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{job_execution_profile: {
<b>"profile_name":<String_value></b>,
"id":<String_value>,
"template_info":<eventrule_configuration_template_value>,
"on_error":<String_value>,
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"description":<String_value>,
"type":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"device":<String_value>,
"device_group":<String_value>,
"parent_id":<String_value>,
"id":<String_value>}],
"display_name":<String_value>}],
"job_name":<String_value>,
"instance_type":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "job_execution_profile":[{
"tenant_id":<String_value>,
"job_name":<String_value>,
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
"template_info":<eventrule_configuration_template_value>,
"id":<String_value>,
"on_error":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/job_execution_profile/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/job_execution_profile

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "job_execution_profile":[{
"tenant_id":<String_value>,
"job_name":<String_value>,
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
"template_info":<eventrule_configuration_template_value>,
"id":<String_value>,
"on_error":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/job_execution_profile/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "job_execution_profile":[{
"tenant_id":<String_value>,
"job_name":<String_value>,
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
"template_info":<eventrule_configuration_template_value>,
"id":<String_value>,
"on_error":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/job_execution_profile/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{job_execution_profile:{
<b>"id":<String_value></b>,
"template_info":<eventrule_configuration_template_value>,
"on_error":<String_value>,
"variables":[{
<b>"name":<String_value></b>,
"parent_id":<String_value>,
"default_value":<String_value>,
"id":<String_value>,
"values_enum_db":<String_value>,
"parent_name":<String_value>,
"value":<String_value>,
"description":<String_value>,
"type":<String_value>,
"device_values":[{
"parent_name":<String_value>,
"value":<String_value>,
"device":<String_value>,
"device_group":<String_value>,
"parent_id":<String_value>,
"id":<String_value>}],
"display_name":<String_value>}],
"job_name":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "job_execution_profile":[{
"tenant_id":<String_value>,
"job_name":<String_value>,
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
"template_info":<eventrule_configuration_template_value>,
"id":<String_value>,
"on_error":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>}]}
```







