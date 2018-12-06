#mps



Configuration for System Status resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>maps_apikey</td><td>&lt;String></td><td>Read-write</td><td>Maps API Key.</td></tr><tr><td>is_cloud</td><td>&lt;Boolean></td><td>Read-write</td><td>True if its a cloud deployment.</td></tr><tr><td>is_member_of_default_group</td><td>&lt;Boolean></td><td>Read-write</td><td>Is Member Of Default Group.</td></tr><tr><td>deployment_type</td><td>&lt;String></td><td>Read-write</td><td>Indicates the type of deployment of MAS: standalone or ha or scaleout..</td></tr><tr><td>is_passive</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates the node's state: ACTIVE or PASSIVE in a HA deployment..</td></tr><tr><td>privilege_feature</td><td>&lt;String></td><td>Read-write</td><td>privilege_feature.</td></tr><tr><td>upgrade_agent_version</td><td>&lt;String></td><td>Read-write</td><td>Indicates the next version the agent needs to upgrade to..</td></tr><tr><td>build_number_short</td><td>&lt;String></td><td>Read-only</td><td>Build Number without Date.</td></tr><tr><td>current_time</td><td>&lt;Integer></td><td>Read-only</td><td>Current Time.</td></tr><tr><td>sysid</td><td>&lt;String></td><td>Read-only</td><td>System Id.</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-only</td><td>Host name on which system is running.</td></tr><tr><td>bios_version</td><td>&lt;String></td><td>Read-only</td><td>BIOS Version.</td></tr><tr><td>hostid</td><td>&lt;String></td><td>Read-only</td><td>Host Id.</td></tr><tr><td>product_version</td><td>&lt;String></td><td>Read-only</td><td>Product Version.</td></tr><tr><td>uptime</td><td>&lt;String></td><td>Read-only</td><td>Uptime.</td></tr><tr><td>current_user_permission</td><td>&lt;String></td><td>Read-only</td><td>This property will show the permission type for current user.</td></tr><tr><td>platform</td><td>&lt;String></td><td>Read-only</td><td>Platform.</td></tr><tr><td>hypervisor_uptime</td><td>&lt;String></td><td>Read-only</td><td>Hypervisor Uptime.</td></tr><tr><td>product_build_number</td><td>&lt;String></td><td>Read-only</td><td>Product Build Number.</td></tr><tr><td>serial</td><td>&lt;String></td><td>Read-only</td><td>Serial Number.</td></tr><tr><td>host</td><td>&lt;String></td><td>Read-only</td><td>Host IP Address on which system is running, this will set for each client session only.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>User Name who is currently connected to the system.</td></tr><tr><td>current_tenant</td><td>&lt;String></td><td>Read-only</td><td>Current Tenant Name for logged-in user.</td></tr><tr><td>time_zone_offset</td><td>&lt;Integer></td><td>Read-only</td><td>Time zone offset in minutes (Example:-330).</td></tr><tr><td>build_number</td><td>&lt;String></td><td>Read-only</td><td>Build Number.</td></tr><tr><td>current_time_formatted</td><td>&lt;String></td><td>Read-only</td><td>Current Time (Formatted).</td></tr><tr><td>time_zone</td><td>&lt;String></td><td>Read-only</td><td>Server Time Zone.</td></tr><tr><td>product</td><td>&lt;String></td><td>Read-only</td><td>Product Name.</td></tr><tr><td>current_tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Current Tenant Id for logged-in user.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[REBOOT](#r)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###reboot







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps?action=reboot;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{"mps": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps":[{
"maps_apikey":<String_value>,
"build_number_short":<String_value>,
"is_cloud":<Boolean_value>,
"current_time":<Integer_value>,
"sysid":<String_value>,
"hostname":<String_value>,
"bios_version":<String_value>,
"hostid":<String_value>,
"is_member_of_default_group":<Boolean_value>,
"product_version":<String_value>,
"deployment_type":<String_value>,
"uptime":<String_value>,
"current_user_permission":<String_value>,
"platform":<String_value>,
"is_passive":<Boolean_value>,
"hypervisor_uptime":<String_value>,
"product_build_number":<String_value>,
"serial":<String_value>,
"privilege_feature":<String_value>,
"host":<String_value>,
"username":<String_value>,
"current_tenant":<String_value>,
"time_zone_offset":<Integer_value>,
"build_number":<String_value>,
"current_time_formatted":<String_value>,
"time_zone":<String_value>,
"upgrade_agent_version":<String_value>,
"product":<String_value>,
"current_tenant_id":<String_value>}]}
```







