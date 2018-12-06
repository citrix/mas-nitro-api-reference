#tenant_system_info



Configuration for This provides the FTU state of the user resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>services_subscribed</td><td>&lt;String></td><td>Read-write</td><td>Services Entitled By the user.</td></tr><tr><td>ftu_state</td><td>&lt;Integer></td><td>Read-write</td><td>Ftu state of the tenant.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>user logged in.</td></tr><tr><td>agent_download_state</td><td>&lt;Integer></td><td>Read-write</td><td>Agent download state.</td></tr><tr><td>services_subscribed_list_arr</td><td>&lt;String[]></td><td>Read-write</td><td>Subscribed Services list.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Id of the parent tenant.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-only</td><td>Id is system generated key for all the syslog generic record..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant_system_info?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{tenant_system_info: {
"services_subscribed_list_arr":<String_value[]>,
"agent_download_state":<Integer_value>,
"username":<String_value>,
"ftu_state":<Integer_value>,
"services_subscribed":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant_system_info":[{
"services_subscribed":<String_value>,
"tenant_id":<String_value>,
"ftu_state":<Integer_value>,
"id":<String_value>,
"username":<String_value>,
"agent_download_state":<Integer_value>,
"services_subscribed_list_arr":<String_value>}]}
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant_system_info

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant_system_info":[{
"services_subscribed":<String_value>,
"tenant_id":<String_value>,
"ftu_state":<Integer_value>,
"id":<String_value>,
"username":<String_value>,
"agent_download_state":<Integer_value>,
"services_subscribed_list_arr":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant_system_info/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant_system_info":[{
"services_subscribed":<String_value>,
"tenant_id":<String_value>,
"ftu_state":<Integer_value>,
"id":<String_value>,
"username":<String_value>,
"agent_download_state":<Integer_value>,
"services_subscribed_list_arr":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant_system_info/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{tenant_system_info:{
"services_subscribed_list_arr":<String_value[]>,
"agent_download_state":<Integer_value>,
"username":<String_value>,
"ftu_state":<Integer_value>,
"services_subscribed":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant_system_info":[{
"services_subscribed":<String_value>,
"tenant_id":<String_value>,
"ftu_state":<Integer_value>,
"id":<String_value>,
"username":<String_value>,
"agent_download_state":<Integer_value>,
"services_subscribed_list_arr":<String_value>}]}
```







