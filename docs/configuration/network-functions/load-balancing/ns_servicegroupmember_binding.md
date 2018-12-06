#ns_servicegroupmember_binding



Configuration for NetScaler Service Group Member Bindings resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip</td><td>&lt;String></td><td>Read-write</td><td>Server IP.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>state.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>customserverid</td><td>&lt;String></td><td>Read-write</td><td>CustomServerID.</td></tr><tr><td>weight</td><td>&lt;String></td><td>Read-write</td><td>Weight.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>servicegroupname</td><td>&lt;String></td><td>Read-write</td><td>Service Group Name.</td></tr><tr><td>svrstate</td><td>&lt;String></td><td>Read-write</td><td>Server State.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Server Port.</td></tr><tr><td>serverid</td><td>&lt;String></td><td>Read-write</td><td>ServerID.</td></tr><tr><td>servername</td><td>&lt;String></td><td>Read-write</td><td>ServerName.</td></tr><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>Save configuration after enable/disable.</td></tr><tr><td>delay</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, allocated to the NetScaler appliance for a graceful shutdown of the service.</td></tr><tr><td>svc_grp_id</td><td>&lt;String></td><td>Read-write</td><td>Service Group ID.</td></tr><tr><td>graceful</td><td>&lt;Boolean></td><td>Read-write</td><td>Graceful shutdown of Service..</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-only</td><td>Host name of the Managed device .</td></tr><tr><td>poll_time</td><td>&lt;Integer></td><td>Read-only</td><td>Last Polling Time.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-only</td><td>Display Name.</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-only</td><td>Comment.</td></tr><tr><td>partition_name</td><td>&lt;String></td><td>Read-only</td><td>Partition Name.</td></tr><tr><td>hash_id</td><td>&lt;String></td><td>Read-only</td><td>Hash Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ENABLE](#e)| [POLL]()| [GET](#get)| [DISABLE](#di)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###enable







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_servicegroupmember_binding?action=enable;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_servicegroupmember_binding: {
<b>"id":<String_value></b>,
"ip":<String_value>,
"delay":<Double_value>,
"ns_ip_address":<String_value>,
"state":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"save_config":<Boolean_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"svc_grp_id":<String_value>,
"port":<Integer_value>,
"serverid":<String_value>,
"servername":<String_value>,
"graceful":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_servicegroupmember_binding":[{
"ip":<String_value>,
"hostname":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"id":<String_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"poll_time":<Integer_value>,
"port":<Integer_value>,
"display_name":<String_value>,
"serverid":<String_value>,
"servername":<String_value>,
"comment":<String_value>,
"partition_name":<String_value>,
"hash_id":<String_value>,
"save_config":<Boolean_value>,
"delay":<Double_value>,
"svc_grp_id":<String_value>,
"graceful":<Boolean_value>}]}
```







###poll







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_servicegroupmember_binding?action=poll;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_servicegroupmember_binding: {
<b>"id":<String_value></b>,
"ip":<String_value>,
"delay":<Double_value>,
"ns_ip_address":<String_value>,
"state":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"save_config":<Boolean_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"svc_grp_id":<String_value>,
"port":<Integer_value>,
"serverid":<String_value>,
"servername":<String_value>,
"graceful":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_servicegroupmember_binding":[{
"ip":<String_value>,
"hostname":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"id":<String_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"poll_time":<Integer_value>,
"port":<Integer_value>,
"display_name":<String_value>,
"serverid":<String_value>,
"servername":<String_value>,
"comment":<String_value>,
"partition_name":<String_value>,
"hash_id":<String_value>,
"save_config":<Boolean_value>,
"delay":<Double_value>,
"svc_grp_id":<String_value>,
"graceful":<Boolean_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_servicegroupmember_binding

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_servicegroupmember_binding":[{
"ip":<String_value>,
"hostname":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"id":<String_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"poll_time":<Integer_value>,
"port":<Integer_value>,
"display_name":<String_value>,
"serverid":<String_value>,
"servername":<String_value>,
"comment":<String_value>,
"partition_name":<String_value>,
"hash_id":<String_value>,
"save_config":<Boolean_value>,
"delay":<Double_value>,
"svc_grp_id":<String_value>,
"graceful":<Boolean_value>}]}
```







###disable







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_servicegroupmember_binding?action=disable;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_servicegroupmember_binding: {
<b>"id":<String_value></b>,
"ip":<String_value>,
"delay":<Double_value>,
"ns_ip_address":<String_value>,
"state":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"save_config":<Boolean_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"svc_grp_id":<String_value>,
"port":<Integer_value>,
"serverid":<String_value>,
"servername":<String_value>,
"graceful":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_servicegroupmember_binding":[{
"ip":<String_value>,
"hostname":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"customserverid":<String_value>,
"weight":<String_value>,
"id":<String_value>,
"servicegroupname":<String_value>,
"svrstate":<String_value>,
"poll_time":<Integer_value>,
"port":<Integer_value>,
"display_name":<String_value>,
"serverid":<String_value>,
"servername":<String_value>,
"comment":<String_value>,
"partition_name":<String_value>,
"hash_id":<String_value>,
"save_config":<Boolean_value>,
"delay":<Double_value>,
"svc_grp_id":<String_value>,
"graceful":<Boolean_value>}]}
```







