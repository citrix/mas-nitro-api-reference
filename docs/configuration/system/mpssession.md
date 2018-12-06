#mpssession



Configuration for Client Session resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tenant_name</td><td>&lt;String></td><td>Read-write</td><td>Tenant Name.</td></tr><tr><td>permission</td><td>&lt;String></td><td>Read-write</td><td>Permission to identify who created the session.</td></tr><tr><td>is_external_auth</td><td>&lt;Boolean></td><td>Read-write</td><td>Is session created by using external authentication.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the client sessions.</td></tr><tr><td>expire_after</td><td>&lt;Integer></td><td>Read-only</td><td>Session will expire after these many seconds.</td></tr><tr><td>login_time</td><td>&lt;Integer></td><td>Read-only</td><td>Session was initiated at this time.</td></tr><tr><td>session_timeout</td><td>&lt;Integer></td><td>Read-only</td><td>Session Timeout set for this session.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Port from where this session was initiated.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>User Name who initiated this session.</td></tr><tr><td>client_type</td><td>&lt;String></td><td>Read-only</td><td>Client Type.</td></tr><tr><td>last_activity_time</td><td>&lt;Integer></td><td>Read-only</td><td>Last Activity Time for this session.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-only</td><td>IP Aaddress from where this session was initiated.</td></tr><tr><td>is_self</td><td>&lt;Boolean></td><td>Read-only</td><td>true, if this session is for current logged-in user.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [DELETE](#delete)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpssession

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpssession":[{
"tenant_name":<String_value>,
"expire_after":<Integer_value>,
"login_time":<Integer_value>,
"permission":<String_value>,
"session_timeout":<Integer_value>,
"port":<Integer_value>,
"username":<String_value>,
"client_type":<String_value>,
"last_activity_time":<Integer_value>,
"session_creator":<String_value>,
"is_external_auth":<Boolean_value>,
"id":<String_value>,
"ip_address":<String_value>,
"token":<String_value>,
"sessionid":<String_value>,
"is_self":<Boolean_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpssession/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpssession":[{
"tenant_name":<String_value>,
"expire_after":<Integer_value>,
"login_time":<Integer_value>,
"permission":<String_value>,
"session_timeout":<Integer_value>,
"port":<Integer_value>,
"username":<String_value>,
"client_type":<String_value>,
"last_activity_time":<Integer_value>,
"session_creator":<String_value>,
"is_external_auth":<Boolean_value>,
"id":<String_value>,
"ip_address":<String_value>,
"token":<String_value>,
"sessionid":<String_value>,
"is_self":<Boolean_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpssession/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







