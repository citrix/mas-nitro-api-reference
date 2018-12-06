#ns_filterpolicy_template



Configuration for NS Filter Policy Configure Task resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Integer></td><td>Read-write</td><td>Policy Priority.</td></tr><tr><td>device_groups</td><td>&lt;String[]></td><td>Read-write</td><td>Device Group Array on which for which template is applied.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of Policy.</td></tr><tr><td>variables</td><td>&lt;variable_values[]></td><td>Read-write</td><td>Values of Variables used in commands of the configuration template.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the Policy: enabled/disabled.</td></tr><tr><td>devices</td><td>&lt;String[]></td><td>Read-write</td><td>Device IP Address Array on which template is applied.</td></tr><tr><td>actionType</td><td>&lt;String></td><td>Read-write</td><td>Action Type of the Policy.</td></tr><tr><td>actionName</td><td>&lt;String></td><td>Read-write</td><td>Action Name of the Policy.</td></tr><tr><td>expression</td><td>&lt;String></td><td>Read-write</td><td>Expression of the Policy.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_filterpolicy_template?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_filterpolicy_template: {
"priority":<Integer_value>,
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
"state":<String_value>,
"actionType":<String_value>,
"actionName":<String_value>,
"expression":<String_value>,
"device_groups":<String_value[]>,
"name":<String_value>,
"devices":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_filterpolicy_template":[{
"priority":<Integer_value>,
"device_groups":<String_value>,
"name":<String_value>,
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
"state":<String_value>,
"devices":<String_value>,
"actionType":<String_value>,
"actionName":<String_value>,
"expression":<String_value>}]}
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_filterpolicy_template

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_filterpolicy_template":[{
"priority":<Integer_value>,
"device_groups":<String_value>,
"name":<String_value>,
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
"state":<String_value>,
"devices":<String_value>,
"actionType":<String_value>,
"actionName":<String_value>,
"expression":<String_value>}]}
```







